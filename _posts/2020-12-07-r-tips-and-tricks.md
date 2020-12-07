---
toc: true
layout: post
description: "cool stuff I recently learned about R"
categories: [R]
title: "Recent R Learnings"
image: images/recentreading.png
comments: true
---

I recently completed a data mining course using [R Notebooks](https://bookdown.org/yihui/rmarkdown/notebook.html) for all my assignments. This approach allowed me to combine my prose, code, results, and supporting materials into a single file and render the resulting report directly to PDF.

{% include alert.html text="I started rendering to DOC, which I then converted to PDFs. Spare yourself the pain! Going direct to PDF was as easy as [installing TinyTeX](https://bookdown.org/yihui/rmarkdown-cookbook/install-latex.html)." %}

Much like Jupyter Notebooks, the R Notebook format is made up of cells that contain text or code. Text is formatted using [R Markdown](https://rmarkdown.rstudio.com) and the attributes of code cells are managed with

Tips and Tricks:
* The keyboard shortcut for inserting an R code chunk is `Cmd + Option + I` on Mac (`Ctrl + Alt + I` on Windows). This will insert a new chunk at the cursor position _or_ :boom: **split the current chunk**! :boom: :astonished:
* [Convert your R Markdown file to a standard R file](https://bookdown.org/yihui/rmarkdown-cookbook/purl.html), automatically stripping out the prose and results with `knitr::purl(file.Rmd, documentation = 1)`. You can extract just the code, code and chunk headers (the default), or code with text chunks as roxygen comments with `documentation` parameters of 0, 1, and 2, respectively.
* The opposite is also possible [using `spin` to convert R files into R Markdown](https://deanattali.com/2015/03/24/knitrs-best-hidden-gem-spin/). Here roxygen comments are used to add markdown (e.g. `#' this is *markdown*`) or code chunk options (e.g. `#+ load-libraries, include=FALSE`). For example, the following R file...

      ``` r
      #' ## Initialize
      #' Load *required* packages
      #+ load-libraries, include=FALSE
      # Prepare for plotting
      library(ggplot2)
      ```

    when processed with `knitr::spin(spin-me.R, knit = FALSE)` results in the following, saved as `spin-me.Rmd`...

      ``` r
      ## Initialize
      Load *required* packages

      ```{r load-libraries, include=FALSE}
      # Prepare for plotting
      library(ggplot2)
      ```
