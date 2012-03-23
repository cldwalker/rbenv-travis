## Description

Run tests for ruby project in current directory based on its .travis.yml,
translating rvm rubies to rbenv equivalents.  Assumes you have git and are
running on a clean git repository.

## Install

  $ mkdir -p ~/.rbenv/plugins
  $ cd ~/.rbenv/plugins
  $ git clone git://github.com/cldwalker/rbenv-travis.git

  # Ping me if you'd like me to gemify this project
  # $ gem install rbenv-travis

## Usage

    $ rbenv travis
    Running before_install...
    Writing new Gemfile to /Users/me/code/gems/boson/Gemfile
    ......................................................................................................................................................................................
    Finished in 0.795336 seconds.

    182 tests, 295 assertions, 0 failures, 0 errors
    ......................................................................................................................................................................................
    Finished in 0.782485 seconds.

    182 tests, 295 assertions, 0 failures, 0 errors

    RESULTS
    *******
    1.9.2-p290: SUCCESS
    1.9.3-p0:   SUCCESS

## About

rbenv-travis uses bundler to isolate gem dependencies from the rest of your system. If
you don't have bundler installed, bundler will be installed. Since rbenv-travis stores
gems locally to bundle/, gitignore bundle/ to speed up installs between runs. After
tests are run, a report is printed and your git repo is cleaned.

## Todo

* Tests!

## Credits

Got this started thanks to awesome @relevance fridays.
