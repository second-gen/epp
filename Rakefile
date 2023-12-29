require 'rubygems'
require 'rake'

begin
  require 'jeweler'

  Jeweler::Tasks.new do |gem|
    gem.name = "epp"
    gem.summary = "EPP (Extensible Provisioning Protocol) for Ruby"
    gem.description = "Basic functionality for connecting and making requests on EPP (Extensible Provisioning Protocol) servers"
    gem.email = "developers@secondgen.com"
    gem.homepage = "http://github.com/second-gen/epp"
    gem.authors = ["Josh Delsman"]

    # Dependencies
    gem.add_development_dependency "shoulda"
    gem.add_development_dependency "mocha"
    gem.add_dependency "hpricot"
    gem.add_dependency "libxml-ruby"
    gem.add_dependency "uuidtools"
  end
rescue LoadError
  puts "Jeweler (or a dependency) not available. Install it with: sudo gem install jeweler"
end

require 'rake/testtask'
Rake::TestTask.new(:test) do |test|
  test.libs << 'lib' << 'test'
  test.pattern = 'test/**/test_*.rb'
  test.verbose = true
end

begin
  require 'rcov/rcovtask'

  Rcov::RcovTask.new do |test|
    test.libs << 'test'
    test.pattern = 'test/**/test_*.rb'
    test.verbose = true
  end
rescue LoadError
  task :rcov do
    abort "RCov is not available. In order to run rcov, you must: sudo gem install spicycode-rcov"
  end
end

task :default => :test
