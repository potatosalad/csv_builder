#!/usr/bin/env rake
require 'bundler/gem_tasks'
require 'rdoc/task'
require 'rspec/core'
require 'rspec/core/rake_task'

desc 'Generate documentation for the csv_builder plugin.'
RDoc::Task.new(:rdoc) do |rdoc|
  rdoc.rdoc_dir = 'rdoc'
  rdoc.title    = 'CSV Builder'
  rdoc.options << '--line-numbers' << '--inline-source'
  rdoc.rdoc_files.include('README.rdoc')
  rdoc.rdoc_files.include('CHANGELOG.rdoc')
  rdoc.rdoc_files.include('lib/**/*.rb')
end

desc 'Test the csv builder'
RSpec::Core::RakeTask.new(:spec) do |t|
  t.pattern   = "./spec/**/*_spec.rb"
end

desc 'Default: run specs.'
task :default => :spec