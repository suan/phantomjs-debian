require 'rubygems'
require 'fpm'

DIR32_LENNY = 'phantomjs-1.6.2-linux-i686-dynamic'
DIR64_LENNY = 'phantomjs-1.7.0-linux-x86_64'
DIR64_WHEEZY = 'phantomjs-1.9.6-linux-x86_64'

desc "Package 32bit Lenny PhantomJS"
task :package32_lenny do
  package DIR32_LENNY, 'i386', '1.6.2-0lenny'
end

desc "Package 64bit Lenny PhantomJS"
task :package64_lenny do
  package DIR64_LENNY, 'x86_64', '1.7.0-0lenny'
end

desc "Package 64bit Wheezy PhantomJS"
task :package64_wheezy do
  package DIR64_WHEEZY, 'x86_64', '1.9.6-0lenny'
end

def package path, arch, version
  puts `fpm -C #{path} -s dir -t deb -n phantomjs -a #{arch} -v #{version} -d libfontconfig1 .`
end
