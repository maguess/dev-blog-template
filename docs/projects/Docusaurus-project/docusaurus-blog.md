# Docusaurus Blog setup
The Docusaurus blog covers the setup documentation, the local build and deployment steps, as well as running the 
project on GitHub as part of the Docusaurus project at the Developer Academy

## Table of Contents
- [Read the checklist](#read-the-checklist)
- [Requirements](#requirements)
  - [Node.js](#nodejs)
  - [GitHub account](#github-account)
  - [IDE](#ide)
- [Installation](#installation)
  - [Installation on GitHub](#installation-on-github)  
  - [Install Git local](#install-git-local)
  - [Test and run](<#test-and-run>)  
- [Changes upon the checklist](#changes-done-upon-to-checklist)
  - [Ignore unrelated files](#ignore-unrelated-files)
  - [Create readme file](#create-readme-file)
  - [Adapt the example.env](#adapt-the-exampleenv)
  - [Adapt the Docusaurus.config.ts](#adapt-the-docusaurusconfigts)
  - [Add a new site logo](#add-a-new-site-logo)
  - [Create a new Markdown file](#create-a-new-markdown-file)
  - [Add the checklist](#add-the-checklist)

# Read the checklist
   First of all take a look to [checklist](docusaurus-lerntagebuch-checkliste.md)

# Prerequisites

import GithubLinkAdmonition from '@site/src/components/GithubLinkAdmonition';

<GithubLinkAdmonition
link="https://github.com/maguess/dev-blog-template.git"
title="Github Tip"
type="tip"
>
Checkout this repository to see the code/implementation
</GithubLinkAdmonition>

## Requirements

### Node.js
```bash
# Download and install fnm:
winget install Schniz.fnm

# In lieu of restarting the shell
fnm env --use-on-cd --shell powershell | Out-String | Invoke-Expression

# Download and install Node.js:
fnm install --use 26

# Verify the Node.js version:
node -v # Should print "v26.13.0".

# Verify npm version:
npm -v # Should print "11.20.0".
```

### GitHub account

register by [gitHub.com](#https://github.com/signup?source=form-home-signup&user_email=)

### IDE
Install any IDE of your choice. (e.g. [Visual Studio Code](#https://code.visualstudio.com/),
[Eclipse](#https://www.eclipse.org/), [IntelliJ](#https://www.jetbrains.com/idea/))

## Installation

### Installation on GitHub

1. Sign in into gitHub.com
2. Look for the template [here](https://github.com/Developer-Akademie-DevSecOpsKurs/dev-blog-template)
3. Use that template to create your repository:
>https://github.com/new?template_name=dev-blog-template&template_owner=Developer-Akademie-DevSecOpsKurs>
4. insert <code>dev-blog-template</code> by Repository name
5. click <code>Create repository</code>
6. you should see the new repository https://github.com/maguess/dev-blog-template

### Install Git local
Change to the desired directory (installation directory).
Test installed git version. If <code>git</code> is not installed then forward with [git](#https://git-scm.com/)

```bash
# change to desired directory:
cd <desired directory>

# check if git is installed:
git --version

# clone the origin-template into your local directory:
git clone https://github.com/Developer-Akademie-DevSecOpsKurs/dev-blog-template.git
```

### Test and run

```bash
# install the project dependencies:
npm install

# test the project:
npm run serve

# run the project:
npm run start
```
If the installation and start has succeeded, then check the browser [here](#http://localhost:3000/dev-blog-template/)

## Changes done upon to checklist

### Ignore unrelated files

This is important to keep your project clean and organized.

- add the name of the file to ignore to the .gitignore file

### Create readme file

- change the readme.md file upon the checklist.

### Adapt the example.env

- change the example.env file upon the checklist.

### Adapt the Docusaurus.config.ts

- change the docusaurus.config.ts file upon the checklist.

### Add a new site logo

- add the logo ![maguess-systems.svg](../../../static/img/maguess-systems.svg)

### Create a new Markdown file

- create a new docusaurus-blog.md file in the [docs/projects/docusaurus-blog.md](/docs/projects/Docusaurus-project/docusaurus-blog.md/docusaurus-blog.md) folder.

### Add the checklist

- add the checklist to the [docusaurus-lerntagebuch-checkliste.md](/docs/projects/Docusaurus-project/docusaurus-lerntagebuch-checkliste.md) file.
