require "bundler/gem_tasks"
require "rake/testtask"

Rake::TestTask.new(:test) do |t|
  t.libs << "test"
  t.libs << "lib"
  t.test_files = FileList["test/**/*_test.rb"]
end

task :default => :test

namespace :docker do
  task :build do
    sh 'docker', 'build', '-t', 'sider/goodcheck:dev', '.'
  end
end
