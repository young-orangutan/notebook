# A Young Orangutan's Notebook

This repository provides a template for a blog/documentation site built from markdown pages. 

The example site is live on https://young-orangutan.github.io/notebook/

## Table of Contents

- [A Young Orangutan's Notebook](#a-young-orangutans-notebook)
  - [Table of Contents](#table-of-contents)
  - [Goals](#goals)
    - [Easy setup](#easy-setup)
    - [Low to no cost](#low-to-no-cost)
    - [To be an improvement over long-form reddit posts](#to-be-an-improvement-over-long-form-reddit-posts)
  - [Deployment Options](#deployment-options)
    - [Manual Deployment](#manual-deployment)
    - [Github Pages](#github-pages)
    - [Just a repository](#just-a-repository)
  - [Prerequisites](#prerequisites)
    - [Development and Testing](#development-and-testing)
    - [Writing](#writing)
  - [Missing Features](#missing-features)

## Goals

### Easy setup

You should be able to get started by copying this repository, removing the posts in the `_posts` directory and adding your own.

### Low to no cost

The result is what is known as a *static site*, which means no database, no logins, just content. This is as cheap to host as it gets (and very fast for users to browse).

Note: you can add interactivity using javascript, but this logic is performed client-side (on the user's computer, not on your servers).

### To be an improvement over long-form reddit posts 

Users who regularly write long-form content and their readers should see an advantage in this approach.

- Posts are written using Markdown, which should be mostly compatible with the reddit syntax
- Git(hub) gives you a full audit history of the changes made to the documents. Versions can be compared and reverted if necessary.
- A reddit post can be deleted, but you and anyone who clones your repository has a backup.
- Better collaboration possibilities 
  - You can invite collaborators and manage their level of permissions
  - Readers can go over your document and send you change requests, if only to correct the occasional typo. You would only have to look at the changes and accept or reject them.
- Relevant files can be stored alongside the documents. I don't give a shit about your screenshot of an excel file with a bunch of financial data. I want the file, so I can open it and analyze it myself. It can easily be included in a repository.
- You can still write a reddit post and link to the repository or website

## Deployment Options

### Manual Deployment

If you want to use a custom webhost, 
1) Clone the repository
2) Run `npm run build` from the commandline. This generates a `_site` folder (not part of the repository)
3) Upload the contents of this folder to your webhost

### Github Pages

Basically, what github does is automate the manual steps above and provide the hosting for free.

1) Go to https://github.com/{your_username}/{your_repository}/settings/pages and set which branch + folder to deploy from
2) Updates to the repository will automatically queue a new deployment
3) Each deployment might take a few minutes before you see changes

### Just a repository

If your repository has a `readme.md` file, it will be rendered at the bottom (just like this one). This applies to each subfolder in the repository. 

This already looks pretty good by itself, so maybe you don't even need a site. Just readmes and subfolders.

## Prerequisites

### Development and Testing

- Ruby - jekyll, the site generator, is a Ruby package. You don't need to know Ruby. I don't either.
- Visual Studio Code for development

- git (installing vscode gives you the option to set up git)
- Node.js

From the commandline,

`npm run build` will generate the site

`npm run test` will allow you to test the site on `localhost:4000/notebook/`. Pages are reloaded as you make changes.

If you copy this repository and deploy your own site, make sure to adjust the urls in `_config.yml`

### Writing

To write a post, you can use any text editor with markdown support.

For Visual Studio Code, I also suggest the [Markdown All in One]([https://](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one)) extension.

You can also use the web-based editor on github. Not the shitty one in the "edit file" option. Press "." somewhere in the repository and use the *real* editor.

Once you commit your updates, the site will be rebuilt.

## Missing Features

This is not yet complete. Notable todos:

- generating a table of outgoing links from a post (like wikipedia's references)
- search
- visual improvements