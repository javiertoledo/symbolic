require 'rubygems'
require 'rake'

begin
  require 'jeweler'
  Jeweler::Tasks.new do |gem|
    gem.name = "symbolic"
    gem.version = '0.3.7'
    gem.summary = 'Symbolic math for ruby'
    gem.description = 'Symbolic math for ruby. This gem can help if you want to get a simplified form of a big equation or to speed up similar calculations or you need an abstraction layer for math. Symbolic does not have any external dependencies. It uses only pure ruby (less than 400 lines of code).'
    gem.email = "ravwar@gmail.com"
    gem.homepage = "http://brainopia.github.com/symbolic"
    gem.authors = ["brainopia"]
    gem.add_development_dependency "rspec", ">= 1.2.9"
    # gem is a Gem::Specification... see http://www.rubygems.org/read/chapter/20 for additional settings
  end
  Jeweler::GemcutterTasks.new
rescue LoadError
  puts "Jeweler (or a dependency) not available. Install it with: sudo gem install jeweler"
end

require 'spec/rake/spectask'
Spec::Rake::SpecTask.new(:spec) do |spec|
  spec.libs << 'lib' << 'spec'
  spec.spec_files = FileList['spec/**/*_spec.rb']
end

Spec::Rake::SpecTask.new(:rcov) do |spec|
  spec.libs << 'lib' << 'spec'
  spec.pattern = 'spec/**/*_spec.rb'
  spec.rcov = true
end

task :spec => :check_dependencies

task :default => :spec