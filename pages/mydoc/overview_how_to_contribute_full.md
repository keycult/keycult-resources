---
title: "How to Contribute - Full Guide"
keywords: contribution guide
tags: [getting_started]
sidebar: mydoc_sidebar
permalink: overview_how_to_contribute_full.html
summary: This page will explain how to get the Jekyll enviornment setup on your local machine, so you can test changes like creating new pages, changing navigation, etc.
---

{% include note.html content="This is the full on guide to contributing large changes to the site. If you only want to make small changes, please see <a href='https://resources.keycult.com/overview_how_to_contribute_small.html'>How to Contribute - Small</a>" %}

This website is created using a simple static website framework called [Jekyll](https://jekyllrb.com/). If you want to develop locally and iterate quickly, it is recommended that you install Jekyll locally on your machine, so that you can test large changes locally before submiting to the repository. This guide will walk you through easily getting your enviornment setup and how to make changes.

## Getting Started

First off, to contribute to the site, you must have a GitHub account. If you dont have one, head over to [GitHub](https://github.com) and create an account. The link to our repository is in the navigation bar at the top. All of our pages are written in Markdown, an easy-to-use markup language. If you are new to Markdown, or need a refresher on syntax, you can view the [Github Markdown guide](https://docs.github.com/en/github/writing-on-github/basic-writing-and-formatting-syntax) for some useful tips and tricks.

## How to Install Jekyll Locall

First thing you need to do is install Jekyll on your machine. This can be done by following the Jekyll specific installation guide for your platform of choice. [Jekyll Install Guide](https://jekyllrb.com/docs/installation/)

## Jekyll Theme Guide

We are using a specifc open-sourced Jekyll theme for this site. The documentation (and a great example of what can be done on the site) is here: [Theme Documentation](https://idratherbewriting.com/documentation-theme-jekyll/index.html)

## Building the site

Once you have the prerequisites installed, clone the repo to your machine. To build the site, run the following command:
```
bundle exec jekyll serve
```
This will build the site, and run it on localhost at port 4000. Open your web browser and navigate to [localhost:4000](http://localhost:4000/). You can now start making changes to the site. As you make changes to the site and modify files, the site will automatically rebuild. Just refresh your web browser to see the latest changes. 

## Quick Development Guide

Now that you have the site up and running, here are a few tips and tricks to get you started.

### 1. Branches