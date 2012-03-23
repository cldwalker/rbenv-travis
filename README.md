## Description

Run tests locally for your ruby project based on its .travis.yml,
translating rvm rubies to rbenv equivalents. Assumes you have git and are
running on a clean git repository.

## Install

    $ mkdir -p ~/.rbenv/plugins
    $ cd ~/.rbenv/plugins
    $ git clone git://github.com/cldwalker/rbenv-travis.git

    # Ping me if you'd like me to gemify this project
    # $ gem install rbenv-travis

## Usage

Start rbenv-travis in a 1.9 ruby:

    $ rbenv travis && echo WOOT
    Writing new Gemfile to /Users/me/code/gems/hirb/Gemfile
    Running tests for 1.8.7-p357...
    ......................................................................................................................................................................................................................

    214 tests, 345 assertions, 0 failures, 0 errors
    Running tests for 1.9.2-p290...
    ......................................................................................................................................................................................................................

    214 tests, 345 assertions, 0 failures, 0 errors
    Running tests for 1.9.3-p0...
    ......................................................................................................................................................................................................................

    214 tests, 345 assertions, 0 failures, 0 errors
    Running tests for jruby-1.6.7...
    ......................................................................................................................................................................................................................

    214 tests, 345 assertions, 0 failures, 0 errors
    Running tests for rbx-2.0.0-dev...
    ......................................................................................................................................................................................................................

    214 tests, 345 assertions, 0 failures, 0 errors

    RESULTS
    *******
    1.8.7-p357: SUCCESS
    1.9.2-p290: SUCCESS
    1.9.3-p0: SUCCESS
    jruby-1.6.7: SUCCESS
    rbx-2.0.0-dev: SUCCESS
    WOOT

## About

rbenv-travis uses bundler to isolate gem dependencies from the rest of your system. If
you don't have bundler installed, bundler will be installed. Since rbenv-travis stores
gems locally to bundle/, gitignore bundle/ to speed up installs between runs. After
tests are run, a report is printed, your git repo is cleaned and exits cleanly only if all
tests pass.

## Todo

* Tests!

## Credits

Got this started thanks to awesome @relevance fridays.
