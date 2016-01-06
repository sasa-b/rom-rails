source 'https://rubygems.org'

gemspec

RAILS_VERSION = '4.2.4'

%w(railties actionview actionpack activerecord).each do |name|
  gem name, RAILS_VERSION
end

gem 'sqlite3', platforms: [:mri, :rbx]
gem 'byebug', platforms: :mri

platforms :jruby do
  gem 'jdbc-sqlite3'
end

group :test do
  gem 'rack-test'
  gem 'rom-sql'
  gem 'rspec-rails', '~> 3.1'
  gem 'codeclimate-test-reporter', require: nil
  gem 'database_cleaner'
  gem 'capybara'
  gem 'generator_spec'
end
