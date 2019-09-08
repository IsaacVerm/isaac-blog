# Jekyll instructions

## Sources

[Programming Historian](https://programminghistorian.org/en/lessons/building-static-sites-with-jekyll-github-pages#what-are-static-sites-jekyll-etc--why-might-i-care-): clear, concise tutorial that got me inspired to experiment with a static site.

## Installation

Jekyll is the static site generator.

Editor used is Visual Code and the Jekyll Snippets and Jekyll Syntax Support are sufficient as extensions.

### Prerequisites

The following need to be installed:

* Homebrew (as package manager but I assume it's installed)
* Ruby (Jekyll is based on Ruby)
* Jekyll
* Bundler (optional if you dont't want to use Jekyll extensions)

### Instructions

Installation follows more or less the [official instructions](https://jekyllrb.com/docs/installation/macos/).

However, Mojave (my Mac OS) poses a problem. The installed version of Ruby on Mojave is 2.3.x (was 2.3.7 in my case). Jekyll requires Ruby 2.4. Luckily there's a way to get the latest Ruby version. Normally you should be able to do this using `homebrew` but I only managed doing it with `rbenv`.

You can install [rbenv](https://amindfulcoder.com/2018/10/08/looking-for-ruby.html) using `homebrew`:

```
brew install rbenv ruby-build
```

Now with `rbenv` installed you can install Ruby:

```
rbenv install 2.6.3
```

I chose Ruby 2.6.3 since that was the last stable version at the type of writing.

Just installing Ruby isn't enough, you also have to [add it to your PATH](https://www.reddit.com/r/MacOS/comments/anw82o/macos_mojave_how_to_install_ruby_successfully/) or else Mojave will keep on using its outdated version of Ruby:

```
echo 'export PATH="/usr/local/opt/ruby/bin:$PATH"' >> ~/.bash_profile
```

Now the latest version Ruby is installed you can install Jekyll and Bundler (package manager Ruby, handy to install Jekyll plugins):

``` 
gem install --user-install bundler jekyll
```

## Running Jekyll

On a first try you first have to create a new [site](https://jekyllrb.com/docs/):

```
jekyll new isaac-blog
```

First remove the `Gemfile.lock` (if one exists) and install the gems needed by Jekyll. I assume you're in the Jekyll site directory (if not run `cd isaac-blog`)

```
rm Gemfile.lock
bundle install
```

Now you can run Jekyll with the installed gems:

```
bundle exec jekyll serve
```