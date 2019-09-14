---
layout: post
title:  "Blog 0: Jekyll, GitHub, Docker"
date:   2019-09-06 18:08:18 -0000
categories: jekyll update
---
Docker

Main purpose of Lab A is installing Docker and setting up environment involving remote procedures. Lab procedures required functional ssh environment, and it was tested by establishing secure connection to the CSUN server: ssh.sandbox.csun.edu. After successful validation of ssh environment, Docker installation stage was started. Remote connection to CSUN server allowed to copy dockerfile needed for further setup of individual accounts on local machine (docker container) and at ssh.sandbox.csun.edu. Docker Desktop was meant to be installed on Windows 10 Home edition. Docker webpage offers package for Windows. However, it is suitable for Windows 10 Pro or Enterprise editions. Installation for Home edition resulting in Installation error message (“Docker Desktop requires Windows 10 Pro or Enterprise version 15063 to run.”). To fix this issue, Docker toolbox (https://docs.docker.com/toolbox/toolbox_install_windows/) provides needed functionality. Docker toolbox package includes:
-	Docker Client for Windows
-	Docker Toolbox management tool and ISO
-	Oracle VM VirtualBox
-	Git MSYS-git UNIX tools
Upon completion of installation process, Docker QuickStart Terminal icon launches a pre-configured Docker Toolbox terminal. Configured terminal displays the $ prompt. The terminal runs bash environment required by Docker. Docker functionality allows to build image ($ docker build …), from that create container ($ docker start cit160), similar to instance of virtual machine.  

Jekyll

Jekyll is an open source software written in Ruby with functionality to generate static web sites. Current stable release is 4.0.0 (2019-08-22). Jekyll website can be found at www.jekyllrb.com. It is multiplatform software. Works on macOS, Linux (and distros), Windows. Requirements include installation of Ruby (2.4.0 or above), Ruby Gems, GCC and Make. Following content describes installation on Windows 10 Home edition. To meet requirements, Ruby and Devkit was installed from rubyinstaller.org/downloads/. Both installers pretty straightforward with clear instructions.  To check Ruby version type ($ruby –v). To check Ruby gems version: $gem –v. To install Jekyll: $gem install Jekyll bundler. To check Jekyll version: $jekyll –v. To create new website for our blog: $jekyll new website name. This command creates website folder in specified directory, along with default content related to static website. To compile and server our website on hosting platform: $bundle exec Jekyll serve. Now website started at localhost address: http://127.0.0.1:4000/. Website can be examined via the browser. Folder _post contains our current and future posts. Folder _site contains final version of website (the ones that will be hosted). Next important file is _config.yml and it contains configurations, variables, and settings for website. Gemfile used by Ruby and contains dependencies for our website: themes, plugins, ruby dependencies.

GitHub

GitHub is platform to perform version control and collaboration. To use this functionality, user need to have and GitHub account. GitHub provides user friendly GUI, as well as functionality of command line by using Git commands. Upon completion setting up account, user should create repository to contain necessary files related to a single project. GitHub feature Branching will allow to work on different version of repository. Original branch will be a master. Second branch will be repo version for experimenting. After successful debugging, validation and testing this branch will be committed to a master branch. Collaboration functionality on GitHub performed via pull and push requests. Pull request means that user offers his edition of repo to being reviewed by other users, and later on to merge them into their branch. Collaborative tools are messages and feedbacks. Most common commands:
-	git init [dir] creates empty repo in specified directory
- git clone <repo> clones repo
-	git status – displays list of files that are staged, unstaged, and untracked
-	git diff – displays unstaged differences between index and working directory
-	git commit – replace last commit with following staged changes and last commit
-	git branch  <branch name> creates new branch with name branch name
-	git checkout –b <branch> creates new branch and checks it out
-	git merge <branch> to merge <branch> into the current branch
-	git pull <remote> - fetch changes from <remote> and merge it with current branch
-	git push <remote> to push local changes to the <remote>

For current assignment, GitHub Pages were used to host Jekyll static website for blog.


[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
