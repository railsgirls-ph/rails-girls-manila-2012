# Deploying Rails Applications

## Getting Started

### Learn Git
-------------------------

Please read the <a href="http://railsgirls.pinoyrb.org/git">Git Guide</a> before anything else.

### Deploy a Rails App on Heroku
-------------------------

Heroku provides the most simple way of deploying a Rails app. All you have to learn is Git.

<a href="http://vimeo.com/53217192" target="_blank">View The Video on How To Deploy a Ruby on Rails Application on Heroku</a>

Download the <a href="https://toolbelt.heroku.com/" target="_blank">Heroku Toolbelt</a>

#### Sign in if you haven't yet.

<pre class="brush: shell">
heroku login
</pre>

#### Create the heroku app

<pre class="brush: shell">
heroku create
</pre>

Rename the app and the URL via heroku.com.

#### Make sure you have the new version of rails

<pre class="brush: shell">
rails -v
Rails 4.0.1
</pre>

Otherwise, please install the latest version of rails.

<pre class="brush: shell">
gem install rails
</pre>

#### Create the rails app

<pre class="brush: shell">
rails new railsgirls
</pre>

Use <a href="http://www.postgresql.org/" target="_blank">postgresql</a> database for production by adding it up as a service on your account. See <a href="https://postgres.heroku.com/" target="_blank">Heroku Postgres</a> for more details.

#### Update the Gemfile

We'll use sqlite3 for development and pg for production.

Change

<pre class="brush: ruby">
 gem 'sqlite3'
</pre>

To

<pre class="brush: ruby">
group :development do
  gem 'sqlite3'
end

group :production do
  gem 'pg'
end
</pre>

Install the gems.

<pre class="brush: shell">
bundle install
</pre>

#### Link to remote repository

<pre class="brush: shell">
git remote add heroku path/to/heroku.git
</pre>


#### Adding config vars on Heroku

We recommend this instead of simply adding password and sensitive information on your config/database.yml file.

Sign in on heroku to view the credentials for your postgresql database.

<pre class="brush: shell">
heroku config:add RG_HOST host
heroku config:add RG_DATABASE database
heroku config:add RG_USER user
heroku config:add RG_PASSWORD password
heroku config:add RG_PORT port
</pre>

Update the app config/database.yml

<pre class="brush: ruby">
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

#### Creating a home page

<pre class="brush: shell">
rm public/index.html
rails g controller Home index
</pre>

#### Updating the routes

Change

<pre class="brush: ruby">
# root :to => 'welcome#index'
</pre>

To

<pre class="brush: ruby">
root :to => 'home#index'
</pre>


Update the text as you wish on app/views/home/index.html.erb

#### Deploying is very simple

#### Add another gem to improve Heroku support for Rails

<pre class="brush: ruby">
group :production do
  gem 'pg'
  gem 'rails_12factor'
end
</pre>

<pre class="brush: shell">
git push heroku master
</pre>

#### Migrations

<pre class="brush: shell">
heroku run rake db:migrate
</pre>

## Credits

<a href ="http://guides.railsgirls.com/heroku/" target="_blank"> Put Your App Online With Heroku</a> by <a href="https://twitter.com/hone02" target="_blank">Terence Lee </a>.


## Contributors to this guide

<a href ="https://blog.bridgeutopiaweb.com" target="_blank"> Katherine G. Pe</a>, software developer.

## Contributing

1. Fork the project at https://github.com/railsgirls-ph/rails-girls-manila-2012
2. Install maruku
<pre class="brush: shell">
gem install maruku
</pre>
3. Make your changes
4. Test your changes
<pre class="brush: shell">
maruku Deploying-Rails-Applications.md
</pre>
5. Commit and create a pull request

