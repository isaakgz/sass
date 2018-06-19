<h1><img width="200px" alt="Sass" src="https://rawgit.com/sass/sass-site/master/source/assets/img/logos/logo.svg" /></h1>

**Sass makes CSS fun again**. Sass is an extension of CSS, adding nested rules,
variables, mixins, selector inheritance, and more. It's translated to
well-formatted, standard CSS using the command line tool or a plugin for your
build system.

```scss
$font-stack: Helvetica, sans-serif;
$primary-color: #333;

body {
  font: 100% $font-stack;
  color: $primary-color;
}

@mixin border-radius($radius) {
  -webkit-border-radius: $radius;
     -moz-border-radius: $radius;
      -ms-border-radius: $radius;
          border-radius: $radius;
}

nav {
  ul {
    margin: 0;
    padding: 0;
    list-style: none;
  }

  li { @include border-radius(10px); }

  a {
    display: block;
    padding: 6px 12px;
    text-decoration: none;
  }
}
```

## Install Sass

You can install Sass on Windows, Mac, or Linux by downloading the package for
your operating system [from GitHub][] and [adding it to your `PATH`][PATH].
That's all—there are no external dependencies and nothing else you need to
install.

[from GitHub]: https://github.com/sass/dart-sass/releases/tag/1.1.1
[PATH]: https://katiek2.github.io/path-doc/

If you use Node.js, you can also install Sass using [npm][] by running

[npm]: https://www.npmjs.com/

```
npm install -g sass
```

**However, please note** that this will install the pure JavaScript
implementation of Sass, which runs somewhat slower than the other options listed
here. But it has the same interface, so it'll be easy to swap in another
implementation later if you need a bit more speed!

See [the Sass website](http://sass-lang.com/install) for more ways to install
Sass.

Once you have Sass installed, you can run the `sass` executable to compile
`.sass` and `.scss` files to `.css` files. For example:

```
sass source/stylesheets/index.scss build/stylesheets/index.css
```

## Learn Sass

Check out [the Sass website](http://sass-lang.com/guide) for a guide on how to
learn Sass!

## This Repository

This repository isn't an implementation of Sass. Those live in
[`sass/dart-sass`][], [`sass/libsass`][], and [`sass/ruby-sass`][]. Instead, it
contains:

[`sass/dart-sass`]: https://github.com/sass/dart-sass
[`sass/libsass`]: https://github.com/sass/libsass
[`sass/ruby-sass`]: https://github.com/sass/ruby-sass

* [`spec/`][], which contains specifications for language features.
* [`proposal/`][], which contains in-progress proposals for changes to the
  language.
* [`accepted/`][], which contains proposals that have been accepted and are
  either implemented or in the process of being implemented.

[`spec/`]: https://github.com/sass/language/tree/master/spec
[`proposal/`]: https://github.com/sass/language/tree/master/proposal
[`accepted/`]: https://github.com/sass/language/tree/master/accepted

Note that this doesn't contain a full specification of Sass. Instead, feature
specifications are written as needed when a new feature is being designed or
when an implementor needs additional clarity about how something is supposed to
work.