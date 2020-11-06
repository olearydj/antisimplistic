---
toc: true
layout: post
description: Notes about using fastpages to build a blog from my Jupyter Notebooks and Markdown documents.
categories: [fastpages, blog, publication, markdown]
title: Blogging with Fastpages
---
# Introduction to Fastpages

This site is built with [fastpages](https://github.com/fastai/fastpages), a platform for building static [Jekyll](https://jekyllrb.com/) web blogs from Jupyter Notebooks. Markdown and Word DOCs are also supported.

![]({{site.baseurl}}/images/diagram.png "https://github.com/fastai/fastpages")

From their github page:

> [fastpages](https://github.com/fastai/fastpages) automates the process of creating blog posts via GitHub Actions, so you don't have to fuss with conversion scripts.  A full list of features can be found on [GitHub](https://github.com/fastai/fastpages).  

Fastpages is built by the [team](https://www.fast.ai/about/) that created the deep learning PyTorch front-end [`fastai`](https://docs.fast.ai) and the Python programming environment [`nbdev`](https://nbdev.fast.ai). The team is led by [Jeremy Howard](https://twitter.com/jeremyphoward), former President and Chief Data Scientist of [Kaggle](https://www.kaggle.com) and author of [_Deep Learning for Coders with Fastai and PyTorch: AI Applications Without a PhD_](https://www.amazon.com/Deep-Learning-Coders-fastai-PyTorch/dp/1492045527)[^1].

Some resources I found helpful in launching this blog:
- The [fastpages github page](https://github.com/fastai/fastpages) has detailed setup instructions
- This [video tutorial](https://youtu.be/L0boq3zqazI) created by [Abdul Majed](https://twitter.com/1littlecoder) walks you through the initial setup process
- A [sample blog page](https://fastpages.fast.ai/fastpages/jupyter/2020/02/21/introducing-fastpages.html) provides a live demonstration of its capabilities


[^1]: Howard, Jeremy, and Sylvain Gugger. Deep Learning for Coders with Fastai and PyTorch. O’Reilly Media, Inc., 2020.





## Basic setup

Jekyll requires blog post files to be named according to the following format:

`YEAR-MONTH-DAY-filename.md`

Where `YEAR` is a four-digit number, `MONTH` and `DAY` are both two-digit numbers, and `filename` is whatever file name you choose, to remind yourself what this post is about. `.md` is the file extension for markdown files.

The first line of the file should start with a single hash character, then a space, then your title. This is how you create a "*level 1 heading*" in markdown. Then you can create level 2, 3, etc headings as you wish but repeating the hash character, such as you see in the line `## File names` above.

## Basic formatting

You can use *italics*, **bold**, `code font text`, and create [links](https://www.markdownguide.org/cheat-sheet/). Here's a footnote[^2]. Here's a horizontal rule:

---

## Lists

Here's a list:

- item 1
- item 2

And a numbered list:

1. item 1
1. item 2

## Boxes and stuff

> This is a quotation

{% include alert.html text="You can include alert boxes" %}

...and...

{% include info.html text="You can include info boxes" %}

## Images

![]({{ site.baseurl }}/images/logo.png "fast.ai's logo")

## Code

You can format text and code per usual

General preformatted text:

    # Do a thing
    do_thing()

Python code and output:

```python
# Prints '2'
print(1+1)
```

    2

Formatting text as shell commands:

```shell
echo "hello world"
./some_script.sh --option "value"
wget https://example.com/cat_photo1.png
```

Formatting text as YAML:

```yaml
key: value
- another_key: "another value"
```


## Tables

| Column 1 | Column 2 |
|-|-|
| A thing | Another thing |


## Tweetcards

{% twitter https://twitter.com/jakevdp/status/1204765621767901185?s=20 %}


## Footnotes



[^2]: This is the footnote.
