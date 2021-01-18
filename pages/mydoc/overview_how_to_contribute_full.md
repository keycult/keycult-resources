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

**main:** As the name implies, this is the main branch of the repository. Any pull requests should be from main. When changes are detected on this branch, the changes are built and deployted.

**gh-pages:** This branch is where the built website content is put after it is built off of the main branch. Changes are automatically pushed to this branch once the content in main is built. You should _not_ submit any code to this branch.

**feature branches:** These are the branches where you can make changes. Create a branch off of master with the following naming `<name>/<change>`. For example: `obsidian/updating-how-to-guide`. This allows a moderator to easily see who has written what branch when going through pull requests.

_Hint:_ To quickly create a branch when you have main checked out, run the following:

To make sure you have the most up to date code
```
git pull                            # make sure you have the most up to date code
```
```
git checkout -b <branch-name>       # will creat a branch with <branch-name>
```
Please make sure that your branch matches the above format described in `feature branches`.

### 2. File Structure

All of the page content is located in the following directory `//pages/mydoc/`. Here you will find the markdown files for each page.

### 3. Editing the Sidebar

The sidebar is described in the YAML file: `//_data/sidebars/mydoc_sidebar.yml`. This file must be edited carefully when updating page content or page order.

## Submitting a Pull Request

Once you have finished the changes that you want to make on your feature branch, it is time to open a pull request. This is usually easist from the GitHub website. Navigate to [the pull request page for this respoitory](https://github.com/keycult/keycult-resources/pulls). You should see your branch with a green button to create a pull request into the `main` branch. Add some information about what you changed, and submit it for approval. Once it passes the automated testing, and is reviewed by the moderation team, it will be merged into `main` and the site will automatically be updated.

## Adding a new page

There are a few things that you need to do to add a new page. Please follow these steps:

### 1. Create your new file

Create a new file for your page with the following format: `//pages/mydoc/<category>_<page-name>`. For example this page name is `//pages/mydoc/overview_how_to_contribute_full.md`

### 2. Add the following header to your page

```
---
title: "How to Contribute - Full Guide"
keywords: contribution guide
tags: [getting_started]
sidebar: mydoc_sidebar
permalink: overview_how_to_contribute_full.html
summary: This page will explain how to get the Jekyll enviornment setup on your local machine, so you can test changes like creating new pages, changing navigation, etc.
---
```
Fill in the information accordingly. The following fields must be changed:
* `title` - title of this page
* `permalink` - the name of this file, but with the extension `.html`
* `summary` - a summary of the information on your page. This will show up if your link is embedded in somewhere like Discord.

### 3. Add your page to the sidebar:

You must now add your page to the appropriate spot in the sidebar YAML file. Here is the YAML entry for this page:
```
    - title: How to Contribute - Full Guide
      url: /overview_how_to_contribute_full.html
      output: web, pdf
```

### 4. Confirm your changes

Build locally and check [localhost:4000](http://localhost:4000/) to make sure your page is added successfully. You should be able to navigate to your new page using the sidebar.

### 5. Add your content

The hard work is done! Now just add your content to your new page in markdown and you're good to go!