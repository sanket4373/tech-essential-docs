---
title: Fork a new repository
description: Guideline on how to fork a repository
updated: 09-26-2018
version: 1.0
---

### Steps on forking a new repository

1. Fork the repo which you want to work on by pressing fork button on github.com and copy the repository link (using ssh)

2. On your terminal run a clone command to setup the origin:
  `git clone git@github.com:your-username/upstream-repo-name.git`

3. Enter the repository: `cd repo-name`

4. Now we link our local repo to the upstream repo in order to pull changes from there:
 	    `git remote add upstream git@github.com:upstream-repo-name/repo-name.git`

5. Now, verify if the remote is indeed been added by: `git remote -v`
