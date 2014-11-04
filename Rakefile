#!/usr/bin/env rake
require 'bundler/gem_tasks'
require File.expand_path('../lib/chosen-rails/source_file', __FILE__)

desc "Update with gior's Chosen Library"
task 'update-chosen', 'repository_url', 'branch' do |task, args|
  remote = args['repository_url'] || 'https://github.com/gior/chosen'
  branch = args['branch'] || 'master'
  files = SourceFile.new
  files.fetch remote, branch
  files.eject_javascript_class_from_closure
  files.cleanup
end
