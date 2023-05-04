# About

This repo is a public source for my personal <a href="http://shubhamaher.com" target="_blank">blogsite</a>.

The blogsite is built with <a href="http://getpoole.com" target="_blank">Poole</a> for <a href="http://jekyllrb.com" target="_blank">Jekyll</a>.

The theme is a personally-tailored version of <a href="https://github.com/poole/hyde" target="_blank">Hyde</a>.

# Setup History (Gemfile based)

1. 2015 : Win 7  x86?
2. 2022 : Win 10 x64!
3. 2023 : Win 7  x64!

# Setup Details (Latest)

2023 : Win 7 U x64 

Ruby:
$ ruby -v
ruby 2.6.0p0 (2018-12-25 revision 66547) [x64-mingw32]

Gem:
$ gem -v
3.0.1

Bundle:
$ bundle -v
Your RubyGems version (3.0.1) has a bug that prevents `required_ruby_version` from working for Bundler. Any scripts that use `gem install bundler` will break as soon as Bundler drops support for your Ruby version. Please upgrade RubyGems to avoid future breakage and silence this warning by running `gem update --system 3.2.3`
Bundler version 2.4.12

Jekyll:
$ jekyll -v
To use retry middleware with Faraday v2.0+, install `faraday-retry` gem
jekyll 2.1.0

# Setup Steps 

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

# Setup Ref
1. [Install Jekyll on Windows 7](https://jkpark.github.io/blog/install-jekyll-on-windows7/)
2. [Run Jekyll on Windows (~7)](http://jekyll-windows.juthilo.com/)
3. [Jekyll on Windows - Official but for Windows ~10 only](https://jekyllrb.com/docs/installation/windows/)