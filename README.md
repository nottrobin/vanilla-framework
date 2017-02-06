# Vanilla Framework

[![Build Status](https://travis-ci.org/ubuntudesign/vanilla-framework.svg?branch=master)](https://travis-ci.org/ubuntudesign/vanilla-framework)
[![npm version](https://badge.fury.io/js/vanilla-framework.svg)](http://badge.fury.io/js/vanilla-framework)
[![Downloads](http://img.shields.io/npm/dm/vanilla-framework.svg)](https://www.npmjs.com/package/vanilla-framework)
[![devDependency Status](https://david-dm.org/ubuntudesign/vanilla-framework/dev-status.svg)](https://david-dm.org/ubuntudesign/vanilla-framework#info=devDependencies)
[![Chat in #vanilla-framework on Freenode](https://img.shields.io/badge/chat-%23vanilla--framework-blue.svg)](http://webchat.freenode.net/?channels=vanilla-framework)

A simple extensible CSS framework, written in [Sass](http://sass-lang.com/).

Vanilla Framework contains a basic CSS grid and pattern classes, and is designed to be extended either directly or by creating extension themes.

[Project homepage](http://ubuntudesign.github.io/vanilla-framework) | [Documentation](http://ubuntudesign.github.io/vanilla-framework/docs/) |
[Project Task Board](https://waffle.io/ubuntudesign/vanilla-framework)

## Hotlinking

On [the project homepage](http://ubuntudesign.github.io/vanilla-framework), find the link to the latest build to add directly into your markup:

``` html
<link rel="stylesheet" href="https://assets.ubuntu.com/v1/vanilla-framework-version-x.x.x.min.css" />
```

``` yaml
hooks: # Top-level YAML attribute, parallel to `apps`
    upgrade: # Hook name, corresponds to executable name
        plugs: [network] # Or any other plugs required by this hook
```

``` python
from fish.chips import MyLunch

class SomeClass:
  arg_one: "hello"

  def a_method(argument, argument2=value):
    """
    Docstring
    """

    variable = "string"
    another = 123

    if some_condition >= 20 and x == y:
      print "go away"
```

## Local usage

Install all the dependancies for vanilla framework project:

``` bash
npm install
```

Then reference it from your own Sass files, with optional settings:

 ```javascript
gulp.task('sass', function() {
  return gulp.src('[your-sass-directory]/**/*.scss')
  .pipe(sass({
    includePaths: ['node_modules']
  }))
});
 ```

 Note: This example uses Gulp but the same principle should apply for your preferred task runner of choice.

``` sass
// Optionally override some settings
$brand-color: #ffffff;

// Import the theme
@import "vanilla-framework/scss/vanilla";

// Run the theme
 @include ubuntu-vanilla-theme;
```

You can override any of the settings in [_global-settings.scss](scss/_global-settings.scss).

If you don't want the whole framework, you can just `@include` specific [modules](scss/modules) - e.g. `@include vf-forms`.

## Themes

- [ubuntu-vanilla-theme](https://github.com/ubuntudesign/ubuntu-vanilla-theme) (alpha)
- [canonical-vanilla-theme](https://github.com/ubuntudesign/canonical-vanilla-theme) (alpha)

## Community

Keep up to date with all new developments and upcoming changes with Vanilla.

- Follow us on Twitter [@UbuntuDesigners](http://twitter.com/ubuntudesigners)
- Read our latest blog posts at [Canonical Blog](http://design.canonical.com/topic/development/)
- Talk to the team in IRC on <code>irc.freenode.com</code> and join channel <code>#vanilla-framework</code>

Code licensed [LGPLv3](http://opensource.org/licenses/lgpl-3.0.html) by [Canonical Ltd.](http://www.canonical.com/).

With ♥ from Canonical
