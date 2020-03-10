---
title: "Flextable Tutorial"
output: html_document
---


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

## Inputs

* Flextable converts an existing data frame into a flextable.
* All of the relevant data must be in the data frame prior to processing.


<pre><code>
myDoc <- myDoc %>%
  body_add_flextable( myFlexTable) 
</code><pre> 


<pre><code>
myDoc <- myDoc %>%
  body_add_fpar(fpar_) %>%
  body_add_flextable( myFlexTable) %>% body_end_section_landscape()
  
</code><pre>  
  
<pre><code>
myQIdoc <- myQIdoc %>%
  body_add_fpar(fpar_) %>%
  body_add_flextable(Make_QI_Table) %>% body_end_section_landscape()
  
</code><pre>   

## Specifying Table Settings

<pre><code>
big_border = fp_border(color="darkgreen", width = 2)
border_v = fp_border(color="gray")
border_h = fp_border(color="gray")

</code></pre>
