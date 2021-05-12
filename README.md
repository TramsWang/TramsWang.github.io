# Dev Instructions

## 1. Install Jekyll and Relatives

Install Ruby and dependencies

```sh
sudo apt install ruby-full build-essential zlib1g-dev
```

Then add following environment variables to `.bashrc`

```sh
# Install Ruby Gems to ~/gems
export GEM_HOME="$HOME/gems"
export PATH=$HOME/gems/bin:$PATH
```

Enable the modification

```sh
source .bashrc
```

Then install Jekyll & Bundler

```sh
gem install jekyll bundler
```

## 2. Build & Test Locally

Navigate to the source root of the site.

Initiate project

```sh
bundle init
```

Add following lines to `Gemfile`

```sh
gem "jekyll"
```

Then there are 2 options:

1. Build only:

   Builds the site and outputs a static site to a directory called `_site`.

   ```sh
   jekyll build
   ```

2. Build & Monitor:

   Does `jekyll build` and runs it on a local web server at `http://localhost:4000`, rebuilding the site any time you make a change.

   ```sh
   jekyll serve
   ```

   Or the following command (This restricts your Ruby environment to only use gems set in your `Gemfile`)
   
   ```sh
   bundle exec jekyll serve
   ```
   
   

