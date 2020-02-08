source 'https://rubygems.org'
git_source(:github) { |repo| "https://github.com/#{repo}.git" }

ruby '2.7.0'

# New Added 2/9/2020 >>> Start

# This line reads the ruby version out of the .ruby-version file, strips off
# any patch level, and then sets it using Bundler's "ruby" directive. This will
# cause bundler to raise an exception if any bundled script is run with a
# different version of Ruby.
ruby_version = IO.readlines(".ruby-version")[0]
version_parts = ruby_version.split('-')
if version_parts.size >= 2 && version_parts[0] == 'ruby'
  # Handles a case where we are prefixing the .ruby-version with ruby-, which
  # is the syntax used by RVM (on our servers)
  ruby version_parts[1].strip
else
  ruby version_parts[0].strip
end

# Trailblazer framework on top of rails
# # (https://github.com/apotonick/trailblazer)
gem 'trailblazer'

## Single responsibility libraries:

# Pundit handles authorization (who can see/do what):
gem "pundit"
# Gives us access to rails responders #respond_with, etc.
gem "responders"
# Roar gives us representers (https://github.com/apotonick/roar)
gem "roar-rails"

## Rails Front-End UI compontents:

# Cells comes from the same guy who makes Trailblazer, and provides better ways
# of data mapping to views. See https://github.com/apotonick/cells
gem "cells"
# Use jquery as the JavaScript library
gem 'jquery-rails'
# Turbolinks makes following links in your web application faster. Read more: https://github.com/rails/turbolinks
gem 'turbolinks'

## Include bootstrap files:
#gem 'bootstrap-sass', '~> 3.3.5'
gem 'sassc'
# Simple form, form helpers with support for bootstrap styling.
gem 'simple_form'

# bundle exec rake doc:rails generates the API under doc/api.
gem 'sdoc', '~> 0.4.0', group: :doc


# Haml support for cells, and dependent pre-released haml
gem 'cells-haml'
gem "haml", github: "haml/haml", ref: "7c7c169"





# New Added 2/9/2020 >>> End

# Bundle edge Rails instead: gem 'rails', github: 'rails/rails'
gem 'rails', '~> 6.0.2', '>= 6.0.2.1'
# Use postgresql as the database for Active Record
gem 'pg', '>= 0.18', '< 2.0'
# Use Puma as the app server
gem 'puma', '~> 4.1'
# Use SCSS for stylesheets
gem 'sass-rails', '>= 6'
# Transpile app-like JavaScript. Read more: https://github.com/rails/webpacker
gem 'webpacker', '~> 4.0'
# Use Redis adapter to run Action Cable in production
# gem 'redis', '~> 4.0'
# Use Active Model has_secure_password
# gem 'bcrypt', '~> 3.1.7'

# Use Active Storage variant
# gem 'image_processing', '~> 1.2'

# Reduces boot times through caching; required in config/boot.rb
gem 'bootsnap', '>= 1.4.2', require: false

group :development, :test do
  # Call 'byebug' anywhere in the code to stop execution and get a debugger console
  gem 'byebug', platforms: [:mri, :mingw, :x64_mingw]
end

group :development do
  # Access an interactive console on exception pages or by calling 'console' anywhere in the code.
  gem 'web-console', '>= 3.3.0'
  gem 'listen', '>= 3.0.5', '< 3.2'
  # Spring speeds up development by keeping your application running in the background. Read more: https://github.com/rails/spring
  gem 'spring'
  gem 'spring-watcher-listen', '~> 2.0.0'
end

group :test do
  # Adds support for Capybara system testing and selenium driver
  gem 'capybara', '>= 2.15'
  gem 'selenium-webdriver'
  # Easy installation and use of web drivers to run system tests with browsers
  gem 'webdrivers'
end

# Windows does not include zoneinfo files, so bundle the tzinfo-data gem
gem 'tzinfo-data', platforms: [:mingw, :mswin, :x64_mingw, :jruby]
