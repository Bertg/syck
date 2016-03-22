require 'bundler/gem_tasks'
require 'rake/extensiontask'
require 'rake/testtask'

CLEAN = Rake::FileList["lib/syck.[so|bundle]", "tmp"]

Rake::TestTask.new(:test) do |t|
  t.libs << "test"
  t.libs << "lib"
  t.test_files = FileList['test/**/test_*.rb']
end
Rake::ExtensionTask.new('syck')

task :default => [:compile, :test]
