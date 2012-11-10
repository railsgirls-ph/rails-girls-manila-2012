# Deploying Rails Applications

## Getting Started

### Learn Git
-------------------------

Please read the <a href="http://railsgirls.pinoyrb.org/git">Git Guide</a> before anything else.

### Deploy a Rails App on Heroku
-------------------------

Heroku provides the most simple way of deploying a Rails app. All you have to learn is Git.

<a href="https://vimeo.com/53217192">Click here to view the video</a>

Download the <a href="https://toolbelt.heroku.com/" target="_blank">Heroku Toolbelt</a>

#### Sign in if you haven't yet.

<pre>
heroku login
</pre>

#### Create the heroku app

<pre>
heroku create
</pre>

Rename the app and the URL via heroku.com.

#### Create the rails app

<pre>
rails new railsgirls
</pre>

Use <a href="http://www.postgresql.org/" target="_blank">postgresql</a> database for production by adding it up as a service on your account. See <a href="https://postgres.heroku.com/" target="_blank">Heroku Postgres</a> for more details.

#### Update the Gemfile

We'll use sqlite3 for development and pg for production.


<pre>
group :development do
  gem 'sqlite3'
end

group :production do
  gem 'pg'
end
</pre>

Install the gems.

<pre>
bundle install
</pre>

#### Adding config vars on Heroku

We recommend this instead of simply adding password and sensitive information on your config/database.yml file.

Sign in on heroku to view the credentials for your postgresql database.

<pre>
heroku config:add RG_HOST host
heroku config:add RG_DATABASE database
heroku config:add RG_USER user
heroku config:add RG_PASSWORD password
heroku config:add RG_PORT port
</pre>

Update the app config/database.yml

<pre>

production:
  adapter: postgresql
  encoding: unicode
  host: ENV['RG_HOST']
  database: ENV['RG_DATABASE']
  pool: 5
  username:	ENV['RG_USER']
  password: ENV['RG_PASSWORD']
  port: ENV['RG_PORT']
</pre>

#### Deploying is very simple

<pre>
git push origin master
</pre>


## Contributors to this guide

<a href ="https://blog.bridgeutiopiaweb.com" target="_blank"> Katherine G. Pe</a>, software developer.


## Contributing

<a href ="https://github.com/railsgirls-ph/rails-girls-manila-2012" target="_blank"> Fork the project and create a pull request if you have some changes</a>