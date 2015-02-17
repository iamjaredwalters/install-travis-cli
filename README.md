# install-travis-cli
Travis CLI hangs when installing on osx.  Follow these commands to successfully install

## Try this first:

### Mac OS X

If you start with a clean Mac OS X, you will have to install the XCode Command Line Tools, which are necessary for installing native extensions. You can do so via xcode-select:

$ xcode-select --install
Mac OS X 10.9.2 shipped with a slightly broken Ruby version. If you want to install the gem via the system Ruby and you get an error, you might have to run the following instead:

$ ARCHFLAGS=-Wno-error=unused-command-line-argument-hard-error-in-future gem install travis

## If that fails use this:
### Instructions (from: https://github.com/travis-ci/travis-ci/issues/2055)


* curl -sSL https://get.rvm.io | bash -s stable --ruby
* source /Users/matt/.rvm/scripts/rvm
* gem install travis
