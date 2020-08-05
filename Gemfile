# frozen_string_literal: true

source 'https://rubygems.org'
git_source(:github) { |repo_name| "https://github.com/#{repo_name}" }

def gem_available?(name)
  Gem::Specification.find_by_name(name)
rescue Gem::LoadError
  false
rescue StandardError
  Gem.available?(name)
end

# gemspec

group :development do
  gem 'pry'
  gem 'pry-byebug'
  gem 'pry-doc'

  gem 'pry-stack_explorer' if gem_available?('pry-stack_explorer')
end

group :development, :test do
  gem 'rake'
  gem 'reek'
  gem 'rspec'
  gem 'rubocop', require: false
  gem 'rubocop-performance', require: false
  gem 'rubocop-rake', require: false
  gem 'rubocop-rspec', require: false
end
