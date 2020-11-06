---
toc: true
layout: post
description: "Notes about using fastpages to build a blog from my Jupyter Notebooks and Markdown documents."
categories: [fastpages, blog, publication, markdown]
title: "Blogging with Fastpages"
image: images/diagram.png
---
## Introduction to Fastpages

This site is built with [fastpages](https://github.com/fastai/fastpages), a platform for building static [Jekyll](https://jekyllrb.com/) web blogs from Jupyter Notebooks. Markdown and Word DOCs are also supported.

![]({{site.baseurl}}/images/diagram.png "https://github.com/fastai/fastpages")

From their github page:

> [fastpages](https://github.com/fastai/fastpages) automates the process of creating blog posts via GitHub Actions, so you don't have to fuss with conversion scripts.  A full list of features can be found on [GitHub](https://github.com/fastai/fastpages).  

Fastpages is built by the [team](https://www.fast.ai/about/) that created the deep learning PyTorch front-end [`fastai`](https://docs.fast.ai) and the Python programming environment [`nbdev`](https://nbdev.fast.ai). The team is led by [Jeremy Howard](https://twitter.com/jeremyphoward), former President and Chief Data Scientist of [Kaggle](https://www.kaggle.com) and author of [_Deep Learning for Coders with Fastai and PyTorch: AI Applications Without a PhD_](https://www.amazon.com/Deep-Learning-Coders-fastai-PyTorch/dp/1492045527)[^1].

I was first introduced `fastpages` and `nbdev` during the recent [ACM TechTalk](https://learning.acm.org/techtalks), [_It's Time Deep Learning Learned from Software Engineering_](https://webinars.on24.com/acm/howard), presented by Howard and moderated by his collaborator [Hamel Husain](https://twitter.com/hamelhusain).

From [Introducing Fastpages](https://fastpages.fast.ai/fastpages/jupyter/2020/02/21/introducing-fastpages.html):

> fastpages uses nbdev to power the conversion process of Jupyter Notebooks to blog posts. When you save a notebook into the /_notebooks folder of your repository, GitHub Actions applies nbdev against those notebooks automatically. The same process occurs when you save Word documents or markdown files into the _word or _posts directory, respectively.

Some resources I found helpful in launching this blog:
- The [fastpages github page](https://github.com/fastai/fastpages) has detailed setup instructions
- This [video tutorial](https://youtu.be/L0boq3zqazI) created by [Abdul Majed](https://twitter.com/1littlecoder) walks you through the initial setup process
- A [sample jupyter-based blog page](https://fastpages.fast.ai/fastpages/jupyter/2020/02/21/introducing-fastpages.html) provides a live demonstration of its capabilities

I was able to get the initial site live quite quickly with little drama, and have found the process of modifying existing content and publishing new material straightforward so far.

[^1]: Howard, Jeremy, and Sylvain Gugger. Deep Learning for Coders with Fastai and PyTorch. O’Reilly Media, Inc., 2020.
