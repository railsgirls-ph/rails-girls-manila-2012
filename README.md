# Rails Girls Manila

## Overview
-----

<a href="http://railsgirls.com/" target="_blank">Rails Girls</a> is a global effort to help girls learn programming and the Ruby on Rails framework.

This guide is written primarily for Rails Girls Manila participants. It was written for beginners and those who have some experience in programming but have not tried Ruby on Rails.



## Getting Started
-----

### <a href="http://guides.railsgirls.com/install/ target="_blank">Setup Recipe for Rails Girls</a>

The coaches should help in case anything fails.


### Choosing a Relational Database Management System

With ActiveRecord, it's possible to use any popular RDBMS. That includes MySQL, PostgreSQL and SQLite3.

#### MySQL

* For Windows users, please refer to this guide:

  <a href="http://blog.mmediasys.com/2011/07/07/installing-mysql-on-windows-7-x64-and-using-ruby-with-it/" target="_blank"> Installing MySQL on Windows 7</a>

  An alternative is to use <a href="http://www.apachefriends.org/en/xampp.html" target="_blank"> XAMPP</a> instead of RailsInstaller. You might still need to look at the guide above to get MySQL2 gem working.

    // install the MySQL2 Library
    gem install mysql2


* For Ubuntu/ Debian users

    // install MySQL
    sudo apt-get install mysql-server-5.1 libmysqlclient15-dev


    // install the MySQL2 Library
    gem install mysql2

* For Mac OS X users

    // install MySQL
    brew install mysql

  or <a href="http://dev.mysql.com/downloads/mysql/5.1.html" target="_blank">Download from MySQL website</a> and install.


    // install the MySQL2 Library
    gem install mysql2


* For those using RVM (on either Mac or Linux), it would help to upgrade to <a href="http://www.ruby-lang.org/en/news/2012/11/09/ruby-1-9-3-p327-is-released/" target="_blank">Ruby 1.9.3 patchlevel 327</a> if you don't already use it.


    #Upgrade
    rvm get latest
    rvm reinstall 1.9.3


#### PostgreSQL


* For Ubuntu/ Debian users

    //install MySQL
    sudo apt-get install postgresql-client


    // install the PG library
    gem install pg

* For Mac OS X users

    // install PostgreSQL
    brew install posgtresql

    brew info postgresql

   // install the PG library

    gem install pg



### Is it working?

You should see errors when you try to start the server.

    rails s



### Learning about environments

We normal work in at least three different environments: **development**, **test** and **production**. Under certain circumstances, another environment called "staging" exists. Rails intuitively gives us the option to add these staging environment by replicating the production environment.



## Organizers and Partners

### <a href="http://groups.google.com/group/ruby-phil" target="_blank">Philippine Ruby Users Group</a>

### <a href="http://devcon.ph/" target="_blank">DevCon</a>
#### <a href="http://webgeek.ph/"  target="_blank">WebGeek Philippines</a>


## Sponsors
---------------------------------------

### <a href="http://aelogica.com/" target="_blank">Aelogica</a>
### <a href="http://smart.com.ph/" target="_blank">SMART Communications, Inc. </a>
#### <a href="http://www.proudcloud.net/" target="_blank">Proudcloud</a>
#### <a href="http://www.sourcepad.com/" target="_blank">SourcePad</a>
#### <a href="http://www.globe.com.ph" target="_blank">Globe Labs</a>
#### <a href="http://www.exist.com/" target="_blank">Exist</a>


