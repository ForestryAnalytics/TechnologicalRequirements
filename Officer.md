---
title: "Officer and Flextable"
output: html_document
---

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
```



### System Requirements

* RStudio
* Java enabled operating systems (e.g. REMSOFTSVR03)

### R package Requirement.

Key R packages for Creating Documents

* Officer
* FlexTable

<pre><code>

library(officer)
library(flextable)
</code></pre>

## Processing a Word Document

### Step 1: Access a template document.

* A Template document can be accessed by using the ``read_docx()`` command, specifying the location and name of the template document.

* **Remark**: for ease of use, the master template document can be divided up into component parts, which would make the insertion of tables into the document easier. 

* For this first step, it is advisable to use the first component of the master termplate (corresponding to the first set of pages.)

<pre><code>

myDoc <- read_docx("myTemplate_Part_A.docx")

</code></pre>

### Step 2: Replacing and editting Text in the document

* Designated Keywords in the template can be replaced with amended values (e.g. specific location names, file references, activity types)
* Designated Keywords MUST NOT include square brackets, as the programme will parse them as regular expressions.

<pre><code>

  myDoc <- myDoc %>% body_replace_all_text("THISSITENAME",mySiteName[i] , only_at_cursor = FALSE)
  myDoc <- myDoc %>% body_replace_all_text("THISFILEREF",myFLRef[i] , only_at_cursor = FALSE)

</code></pre>


### Step 3: Adding Text to the document.

* Text may be added to the document, but it would be unformatted. This would affect the visual appeal of the output.
* For best use, the text should be preformatted with specified settings.
* The commands are ``fpar()`` and ``ftext()``.
* Formatting may be predefined.

<pre><code>

bold_face_1 <- shortcuts$fp_bold(font.size = 24)
bold_face_2 <- shortcuts$fp_bold(font.size = 20)
bold_face_3 <- shortcuts$fp_bold(font.size = 16)
bold_redface <- update(bold_face_1, color = "red")

</code></pre>

The following example shows how to create and format text for a paragraph.

<pre>code>
fpar_title <- fpar(ftext("Appropriate Assessment Screening", prop = bold_face_1))
  

AA_Text_1 <- "The project has been subject to the DAFM's AA Screening procedure, as set out in the document entitled Appropriate Assessment Procedure: Guidance Note & iFORIS SOP for DAFM Forestry Inspectors (v.05Nov19) (DAFM, 2019). The AA Screening report is included on file for this application." 

AA_Text_2 <- "The AA Screening procedure identified all European sites within 15 km of the project area. The potential for an effect on European sites located outside the 15 km was also considered, but no pathways for significant effect were identified. "

AA_Text_3 <- "This process concluded that there was no possibility of the project - either individually or in combination with other plans and projects - having an effect on the following Natura site(s): "
  
  fpar_1 <- fpar(ftext(AA_Text_1,  prop = fp_text(color = "black", font.size = 10, bold = FALSE)))
  fpar_2 <- fpar(ftext(AA_Text_2,  prop = fp_text(color = "black", font.size = 10, bold = FALSE)))
  fpar_3 <- fpar(ftext(AA_Text_3,  prop = fp_text(color = "black", font.size = 10, bold = FALSE)))
</code></pre>    

Now that the text is created and formatted, It can be added to the main document.
<pre><code>  
  myDoc <- myDoc %>%
    body_add_fpar(fpar_title) %>%
    body_add_par("", style = "Normal") %>% 
    body_add_fpar(fpar_1) %>%
    body_add_par("", style = "Normal") %>% 
    body_add_fpar(fpar_2) %>%
    body_add_par("", style = "Normal") %>% 
    body_add_fpar(fpar_3) %>%
    body_add_par("", style = "Normal")
    
</code></pre>    


