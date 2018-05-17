require 'bundler/gem_tasks'
require 'rake/testtask'
require 'find'

desc 'Say Hello'
task :hello do
	puts "Hello There! This is the 'hello' task"
end

desc 'Run Tests'
task :default => :test

Rake::TestTask.new(:test) do |t|
	t.libs << "test"
	t.libs << "lib"
	t.test_files = FileList['test/**/*_test.rb']
end

desc 'Display inventory of all files'
task :inventory do
	Find.find('.') do |name|
		next if name.include?('/.')
		puts name if File.file?(name)
	end
end