# Git
-------------

Git is a version control system, a simple command line tool for keeping a history on the state of your source code projects. You use it as you might use something like Subversion, CVS or Perforce.

## Resources
-------------

### <a href ="http://git-scm.com/book" target="_blank"> Pro Git: A free definitive book written by Scott Chacon</a>
### <a href ="https://github.com/progit/progit" target="_blank"> Pro Git contents updated the community</a>
### <a href ="http://railscasts.com/episodes/96-git-on-rails" target="_blank"> Git on Rails </a>


### Defining a Gitignore
-------------------------

The .gitignore file contains files or folders you want to ignore for a project. These will not be included on the list of files and folders to be tracked for changes and will not be commited. Developers usually ignore temporary files created or probably configuration files.


### Defining a Global Gitignore
-------------------------------

The .global_gitgnore resides on your home directory. If you use Linux or OS X, the file is ~/.global_gitignore

#### Common files and folders to ignore for a Ruby on Rails project

<pre>
*.rbc
*.sassc
.sass-cache
capybara-*.html
.rspec
/.bundle
/vendor/bundle
/log/*
/tmp/*
/db/*.sqlite3
/public/system/*
/coverage/
/spec/tmp/*
**.orig
rerun.txt
pickle-email-*.html
</pre>

For OS X users, we ignore the following files:

<pre>
.DS_Store
.AppleDouble
.LSOverride
Icon


# Thumbnails
._*

# Files that might appear on external disk
.Spotlight-V100
.Trashes
</pre>

Fore more files to ignore, check the <a href="https://github.com/github/gitignore/tree/master/Global" target="_blank">gitignore</a> list updated by several developers worldwide.


## Git Hosting (usually free)
-----------------------------

### <a href ="http://assembla.com/" target="_blank"> Assembla </a>
### <a href ="https://github.com/" target="_blank"> Github </a>



## Setting up git on shared hosting
----------------------

You need an SSH user or a user who can log in to your account via a terminal.

<pre>
ssh user@host

mkdir project
cd project
git --bare init

</pre>

Your git repository link would look like:


<pre>
user@host:~/project
</pre>
