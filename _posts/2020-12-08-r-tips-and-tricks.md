---
toc: true
layout: post
description: "cool stuff I recently learned about R"
categories: [R]
title: "Recent R Learnings"
image: images/recentreading.png
comments: true
hide: true
---

I recently completed a course that used R for various statistical and machine learning methods. In separate articles I discussed the course and my semester project, [Text Sentiment Analysis with R](https://bit.ly/asb-7130-acnw-project), and provided an introduction to R Markdown.

Here I'll focus on how I used R Studio's [markdown-based publication tools](https://rmarkdown.rstudio.com) to integrate my analysis and documentation efforts and render the final results in a variety of formats.

# Course Application

Throughout the course I used [R Notebooks](https://bookdown.org/yihui/rmarkdown/notebook.html) to combine my prose, code, results, and supporting materials into a single file and render the resulting report directly to PDF.

> I started rendering to DOC, which I then converted to PDFs. Spare yourself the pain! Going direct to PDF was as easy as [installing TinyTeX](https://bookdown.org/yihui/rmarkdown-cookbook/install-latex.html).

### Tips and Tricks

**Keyboard Shortcuts**

The keyboard shortcut for inserting an R code chunk is `Cmd + Option + I` on Mac (`Ctrl + Alt + I` on Windows). This will insert a new chunk at the cursor position _or_ :boom: **split the current chunk**! :boom: :astonished:

**Converting Between R and R Markdown**

[Convert your R Markdown file to a standard R file](https://bookdown.org/yihui/rmarkdown-cookbook/purl.html), automatically stripping out the prose and results with `knitr::purl("file.Rmd", documentation = 1)`. You can extract just the code, code and chunk headers (the default), or code with text chunks as roxygen comments with `documentation` parameters of 0, 1, and 2, respectively.

The opposite is also possible [using `spin` to convert R files into R Markdown](https://deanattali.com/2015/03/24/knitrs-best-hidden-gem-spin/). Here roxygen comments are used to add markdown (e.g. `#' this is *markdown*`) or code chunk options (e.g. `#+ load-libraries, include=FALSE`). For example, given the following R file with a mix of comment styles:

``` r
#' ## Initialize
#' *Fun* with `mtcars`!
#+ summary-stats, echo=FALSE
# Summarize mpg
summary(mtcars$mpg)
```

`knitr::spin("spin-me.R", knit = FALSE)` results in the file `spin-me.Rmd`, with two chunks. The first is markdown with a level 2 header and some bold formatted text. The second is an R code chunk named `summary-stats` with `echo=FALSE` that includes a comment:

``` r
## Initialize
*Fun* with `mtcars`!

```{r summary-stats, echo=FALSE}
# Summarize mpg
summary(mtcars$mpg)
```

If you are only interested in publishing your R files, simply omit the `knit = FALSE` parameter from `spin` to go directly to the final rendered output, e.g. md, pdf, etc.

## Twitter

I found several of these on [Brendan Cullen's](https://twitter.com/_bcullen) recent twitter thread:

<center>{% twitter https://twitter.com/_bcullen/status/1333878752741191680 %}</center>
