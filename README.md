## Description

Run tests for ruby project in current directory based on its .travis.yml. Obviously for rbenv-based rubies.

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


## TODO

* Actually get this to work without hardcoded rubies.

## Credits

Got this started thanks to awesome @relevance fridays.
