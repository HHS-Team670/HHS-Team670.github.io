---
title: Git Commands
layout: home
parent: Hardware and Software
nav_order: 2
---

# Git Commands

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

# What is Git?

Git is a version control system that allows you to track changes to files and collaborate on projects. It helps manage code over time and enables people to work together on projects without overwriting each other's changes. 

## What is Version Control?

Version control is a system that records changes made to files over time. It allows you to:
* Keep track of the history of changes.
* Revert to earlier versions if needed.
* Collaborate with others without conflicts by managing changes separately.

Git is a distributed version control system. This means that every developer has a full copy of the entire repository and its history on their own machine.

## Key Concepts

### Repository
A repository (commonly refered to as a repo) is a storage space for a project, where project files and history are stored. It can be local or remote. For example, a version of a repository can be stored on an online server (in this case, Github). 

`git init` — Create empty Git repository.

### Branch
A branch in a repository allows the creation of an independent line of work within a project, enabling work on a project without affecting the main branch.

`git branch <branch>` — Create new branch.
`git checkout <branch>` — Switch to a branch.

### Clone
Cloning creates a local copy of a remote repository, including its history and branches.

`git clone <repository-url>` — Clones the repository from the URL.

### Fetch
Fetching downloads updates from a remote repository to a local machine without immediately updating the local files. 

`git fetch` — Fetch edits from remote repository.

### Pull
Pulling updates a local repository by downloading changes from a remote repository and updating the local files with these changes.

`git pull` — Pull changes from remote repository and updates local files.

### Commit
A commit saves changes made to files in a local repository. When committing, changes are recorded with a descriptive message, which becomes part of the project's version history.

`git commit -m "<message>"` — Commit changes with a descriptive message.

### Push
Pushing involves sending committed changes from a local repository to a remote repository.

`git push` — Push committed changes to remote repository.

### Merge
Merging combines changes from one branch into another.

`git merge <branch>` — Merge a branch to the current branch.

## Other Resources

This page only briefly goes over Git and its commands. For more information, visit the following videos and websites. These are completely optional, but it is recommended to go over the Official Documentation.

* [Official Documentation](https://git-scm.com/doc) 
* [https://www.youtube.com/watch?v=HVsySz-h9r4](https://www.youtube.com/watch?v=HVsySz-h9r4)
* [https://www.youtube.com/watch?v=8JJ101D3knE&ab_channel=ProgrammingwithMosh](https://www.youtube.com/watch?v=8JJ101D3knE&ab_channel=ProgrammingwithMosh)