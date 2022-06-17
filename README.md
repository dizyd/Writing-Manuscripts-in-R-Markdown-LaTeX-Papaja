# Workshop: Writing Manuscripts in R using LaTeX, R Markdown, and `papaja`

This repository contains the materials for the workshop **Writing Manuscripts in R using LaTeX, R Markdown, and `papaja`**. 

The workshop consists of three parts:

- Introduction to $\LaTeX{}$
- Introduction to `R Markdown`
- Writing scientific articles with the [`papaja`](https://github.com/crsh/papaja) package


## The Materials

The slides are in `.html` format and can be found in the corresponding folders. The best way to make sure you have everything is to download this whole github repository by clicking on the green `Code` button and then on `Download ZIP`: 

![screenshot](https://user-images.githubusercontent.com/7207563/139688624-68fd802e-e408-4941-99e8-ef8e898743d6.PNG)


## Packages needed

The following code can be used to install the packages used in this workshop:

```r
wanted.packages <- c("tidyverse","ggplot2","devtools","parameters","gganimate","plotly","kableExtra",
"DT","correlation","corx","palmerpenguins")
  
# Check what packages need to be installed
new.packages <- wanted.packages[!(wanted.packages %in% installed.packages()[,"Package"])]
  
 # install the not yet installed but required packages and load them
if(length(new.packages)) install.packages(new.packages,dependencies = TRUE)
sapply(wanted.packages, require, character.only = TRUE)
```

## Also to be installed:

For the second part of the workshop, you also need to install the [papaja-package](https://github.com/crsh/papaja) and a `TeX` distribution (e.g., MikTeX for Windows, MacTeX for Mac, or TeX Live for Linux) to create .pdf documents. 

If you did install LaTeX before or already created some .pdf documents with R Markdown, you are good to go.   If you have not installed LaTeX before, I recommend installing TinyTeX (https://yihui.name/tinytex/), which is a light and easy-to-maintain LaTeX distribution for R Markdown.



TinyTex can be installed from within R as follows.

```r
if(!"tinytex" %in% rownames(installed.packages())) install.packages("tinytex")

tinytex::install_tinytex()
```

The `papaja`- package then can be installed via 

```r
# Install devtools package if necessary
if(!"devtools" %in% rownames(installed.packages())) install.packages("devtools")

# Install the stable development verions from GitHub
devtools::install_github("crsh/papaja")
```
## For LaTeX: Register @Overleaf

Please register an account at https://www.overleaf.com/, which we will use in the $\LaTeX{}$ part 

<br>
<br>

**Note:** The workshop is based on R Version 4.2.0


