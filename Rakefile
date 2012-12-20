require 'rubygems'
require 'fpm'

DIR32 = 'phantomjs-1.6.2-linux-i686-dynamic'
DIR64 = 'phantomjs-1.7.0-linux-x86_64'

task :default => :package_all

desc "Package 32bit and 64bit Lenny PhantomJS"
task :package_all => [:package32, :package64]

desc "Package 32bit Lenny PhantomJS"
task :package32 do
  package DIR32, 'i386', '1.6.2-0lenny'
end

desc "Package 64bit Lenny PhantomJS"
task :package64 do
  package DIR64, 'x86_64', '1.7.0-0lenny'
end

def package path, arch, version
  puts `cd #{path} && fpm -s dir -t deb -n phantomjs -a #{arch} -v #{version} .`
end
