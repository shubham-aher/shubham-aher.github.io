---
layout: post
title: How to install jekyll on Windows 7 x64
published: true
---

### Intro

Installing jekyll on an outdated Windows 7 OS needs a group of modules(ruby, gem, bundle, jekyll) with a specific matching set of older versions of the dependencies. 

On Windows 10 most of the latest versions of the required modules and gems are compliant with the OS.

Hence for Windows 7 x64, the table below highlights the group of modules with versions that are tried and tested and covered by this guide for a successful jekyll installation :  

### Jekyll on Windows 7 Ultimate x64 :

| Module / Gem / Dependency Name | Version |
| ----------- | ----------- |
| ruby | 2.6.0 { Version string - 2.6.0p0 (2018-12-25 revision 66547) [x64-mingw32] } |
| gem | 3.0.1 |
| bundler | 2.4.12 |
| rogue | 0.1.1 |
| nokogiri | 1.13.10 x64-mingw32 |
| jekyll | 2.1.0 |

Note#1 : The "architecture" used by "mingw" is "x64-mingw32" since its x64 edition of Windows 7.

Note#2 : While installing Ruby+Devkit please opt to install the complete msys2 suite.

This guide is tested on Windows 7 Ultimate x64 with below details: 
```
Microsoft Windows [Version 6.1.7601]
Copyright (c) 2009 Microsoft Corporation.  All rights reserved.

systeminfo | findstr /B /C:"OS Name" /B /C:"OS Version"
OS Name:                   Microsoft Windows 7 Ultimate
OS Version:                6.1.7601 Service Pack 1 Build 7601
```

### Setup Steps 

1. Install Git (Git-2.40.1-64-bit.exe) and checkout [github-pages blog repo](https://github.com/shubham-aher/shubham-aher.github.io). 
2. Install ["Ruby+Devkit 2.6.0-1 (x64)"](https://github.com/oneclick/rubyinstaller2/releases/download/RubyInstaller-2.6.0-1/rubyinstaller-devkit-2.6.0-1-x64.exe) (rubyinstaller-devkit-2.6.0-1-x64.exe) from [Ruby Archives](https://rubyinstaller.org/downloads/archives/)
3. Copy/Paste "gemrc" file from github-pages blog repo to C:\ProgramData\ on Windows.
4. 'set HTTPS_PROXY=https://address:port'
5. 'gem update && gem cleanup'
6. 'gem install jekyll:2.1.0'
7. 'gem install rogue'
8. //Delete existing Gemfile.lock (if last build was done with a different setup combination of OS+Ruby+Gem+Bundle+Jekyll version)
9. 'bundle install' (This will pick Gemfile and parse it to install all dependencies)
10. 'bundle exec jekyll serve'

### Setup References
1. [Install Jekyll on Windows 7](https://jkpark.github.io/blog/install-jekyll-on-windows7/)
2. [Run Jekyll on Windows (~7)](http://jekyll-windows.juthilo.com/)
3. [Jekyll on Windows - Official but for Windows ~10 only](https://jekyllrb.com/docs/installation/windows/)

### Extra Details of Setup

Ruby:
```
$ ruby -v
ruby 2.6.0p0 (2018-12-25 revision 66547) [x64-mingw32]
```

Gem:
```
$ gem -v
3.0.1
```

Bundle:
```
$ bundle -v
Your RubyGems version (3.0.1) has a bug that prevents `required_ruby_version` from working for Bundler. Any scripts that use `gem install bundler` will break as soon as Bundler drops support for your Ruby version. Please upgrade RubyGems to avoid future breakage and silence this warning by running `gem update --system 3.2.3`
Bundler version 2.4.12
```

Jekyll:
```
$ jekyll -v
To use retry middleware with Faraday v2.0+, install `faraday-retry` gem
jekyll 2.1.0
```

Gems Installed :   
```
$ gem list --local
actioncable (5.0.7.2)
actionmailer (5.0.7.2)
actionpack (5.0.7.2)
actionview (5.0.7.2)
activejob (5.0.7.2)
activemodel (5.0.7.2)
activerecord (5.0.7.2)
activesupport (5.0.7.2)
addressable (2.8.4)
arel (7.1.4)
bigdecimal (3.1.4, default: 1.4.1)
blankslate (2.1.2.4)
builder (3.2.4)
bundler (2.4.12, default: 1.17.2)
classifier (1.3.5)
cmath (default: 1.0.0)
coffee-script (2.4.1)
coffee-script-source (1.12.2)
colorator (0.1)
concurrent-ruby (1.2.2)
crass (1.0.6)
csv (3.2.6, default: 3.0.2)
date (3.3.3, default: 1.0.0)
dbm (default: 1.0.0)
did_you_mean (1.6.3)
e2mmap (default: 0.1.0)
erubis (2.7.0)
etc (1.4.2, default: 1.0.1)
execjs (2.8.1)
faraday (2.7.4)
faraday-net_http (3.0.2)
fast-stemmer (1.0.2)
fcntl (1.0.2, default: 1.0.0)
ffi (1.15.5 x64-mingw32)
fiddle (default: 1.0.0)
fileutils (1.7.1, default: 1.1.0)
forwardable (1.3.3, default: 1.2.0)
gdbm (default: 2.0.0)
globalid (1.1.0)
i18n (1.13.0)
io-console (0.6.0, default: 0.4.7)
ipaddr (1.2.5, default: 1.2.2)
irb (default: 1.0.0)
jekyll (2.1.0)
jekyll-coffeescript (1.2.2)
jekyll-gist (1.5.0)
jekyll-paginate (1.1.0)
jekyll-sass-converter (1.5.2)
jekyll-watch (1.5.1)
json (2.6.3, default: 2.1.0)
kramdown (1.17.0)
liquid (2.6.3)
listen (3.8.0)
logger (1.5.3, default: 1.3.0)
loofah (2.20.0)
mail (2.8.1)
mathn (0.1.0)
matrix (0.4.2, default: 0.1.0)
mercenary (0.3.6)
method_source (1.0.0)
mini_mime (1.1.2)
minitest (5.18.0)
mutex_m (0.1.2, default: 0.1.0)
net-imap (0.3.4)
net-pop (0.1.2)
net-protocol (0.2.1)
net-smtp (0.3.3)
net-telnet (0.2.0)
nio4r (2.5.9)
nokogiri (1.13.10 x64-mingw32)
octokit (4.25.1)
openssl (default: 2.1.2)
ostruct (0.5.5, default: 0.1.0)
parslet (1.5.0)
posix-spawn (0.3.15)
power_assert (2.0.3)
prime (0.1.2, default: 0.1.0)
psych (default: 3.1.0)
public_suffix (5.0.1)
pygments.rb (0.6.3)
racc (1.6.2)
rack (2.2.7)
rack-test (0.6.3)
rails (5.0.7.2)
rails-dom-testing (2.0.3)
rails-html-sanitizer (1.5.0)
railties (5.0.7.2)
rake (12.3.2)
rb-fsevent (0.11.2)
rb-inotify (0.10.1)
rdoc (default: 6.1.0)
redcarpet (3.6.0)
reline (0.3.3)
rexml (3.2.5, default: 3.1.9)
rogue (0.1.1)
rss (0.2.9, default: 0.2.7)
ruby2_keywords (0.0.5)
safe_yaml (1.0.5)
sass (3.7.4)
sass-listen (4.0.0)
sawyer (0.9.2)
scanf (default: 1.0.0)
sdbm (default: 1.0.0)
shell (0.8.1, default: 0.7)
singleton (0.1.1)
sprockets (4.2.0)
sprockets-rails (3.2.2)
stringio (3.0.6, default: 0.0.2)
strscan (3.0.6, default: 1.0.0)
sync (default: 0.5.0)
test-unit (3.5.7)
thor (1.2.1)
thread_safe (0.3.6)
thwait (0.2.0, default: 0.1.0)
timeout (0.3.2)
toml (0.1.2)
tracer (0.1.1, default: 0.1.0)
tzinfo (1.2.11)
webrick (1.8.1, default: 1.4.2)
websocket-driver (0.6.5)
websocket-extensions (0.1.5)
xmlrpc (0.3.2)
yajl-ruby (1.2.3)
zlib (3.0.0, default: 1.0.0)
```
