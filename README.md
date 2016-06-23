getchopstick.com website
========================

## Requirements

1. [Ruby](https://www.ruby-lang.org) and [rubygems](https://rubygems.org)
2. [Node 4.4.4](http://nodejs.org) and [npm 2.15.1](https://npmjs.org) or [NVM](https://github.com/creationix/nvm)

## Install

For automated install just run ./install.sh from project root.
This will check if package managers are installed and download required packages for you. For manual installation follow the below method.

You only need to do this once in a new project.
First, `cd` into the project root (where this file is).
Install [bundler](http://bundler.io) and the necessary Ruby dependencies:

    gem update --system && gem install bundler
    bundle install

Install [bower](http://bower.io) and the necessary JavaScript dependencies:

    npm install -g bower
    bower install

Install [gulp](http://gulpjs.com/) and the necessary gulp dependencies:

    npm install -g gulp
    npm install

Project specific code should be written in the components layer.

## Use

We use Gulp as our task runner. There are some basic tasks defined but these can be easily extended by changing the `gulpfile.js`.

To compile Chopstick Boilerplate, `cd` into the project root and run:

    gulp

This will compile the `scss` and build the Jekyll site.

For development there is also a watch task wich will load a browsersync server and watch your all your files (`*.html, *.md, *.scss, *.js, *.jpg, *.png, *.svg`) for changes:

    gulp watch

Browsersync also works as a server for your devices. More info can be found on the [browsersync site](http://www.browsersync.io/).

### Boilerplate

The boilerplate can be used as a **styleguide**, to build **static websites** or to speed up making **HTML prototypes**.

### `.scss` structure.

The Chopstick Scss is maintained in separate repositories which are loaded with [Bower](http://bower.io/). We believe these partials should be easy to update and configurable without writing new code.

#### Partials
We use the following partials according to the [ITCss](http://itcss.io/) structure.
1. [chopstick-settings](https://github.com/getchopstick/chopstick-settings): contains global variables and config switches to get you started. These can be overwritten in your project. Simply duplicate the variables you want to change or replace this file.
2. [chopstick-tools](https://github.com/getchopstick/chopstick-tools):  contains mixins and functions.
3. [chopstick-generic](https://github.com/getchopstick/chopstick-generic): contains ground-zero styles (Normalize.css, resets, box-sizing)
4. [chopstick-elements](https://github.com/getchopstick/chopstick-elements): contains unclassed HTML elements (type selectors)
5. [chopstick-objects](https://github.com/getchopstick/chopstick-objects): contains cosmetic-free design patterns
6. chopstick-components: contains designed components, chunks of UI (these are maintained in the boilerplate as they are specific to this)
6. [chopstick-utilities](https://github.com/getchopstick/chopstick-utilities): contains helper classes

#### Usage
We try to keep the code as modular as possible. So you can comment out what you don’t use.

If you want to change something within the external partials you have 3 options:
1. Change the settings and default appearance by overriding the variables in your project.
2. Create a pull request on the source code in the correct repository.
3. Copy the original file in you own project. This means you will have to do manual updates in the future.

## Credits

You are free to contribute to Chopstick via GitHub Pull Requests. We have a couple of simple guidelines we try to follow, of which most are taken from the [CSS Tricks Sass Style Guide](http://css-tricks.com/sass-style-guide). Please refer to the [CONTRIBUTING.md](https://github.com/getchopstick/chopstick-boilerplate/blob/master/CONTRIBUTING.md) for more information

We owe a ton of credits to the following projects for inspiration:

* [ITCSS](http://itcss.io/)
* [SMACSS](https://smacss.com/)
* [OOCSS](http://oocss.org/)
* [HTML5 Boilerplate](https://html5boilerplate.com/)
* [Inuit CSS](http://inuitcss.com/), [Foundation](http://foundation.zurb.com/) and [Bootstrap](http://getbootstrap.com/)
