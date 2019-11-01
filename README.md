# Pippip v3

Contents:

- [About](#About)
- [Browser support](#browser-support)
- [Setup](#setup)
- [Webpack](#webpack)
- [CSS](#css)
- [Included helper classes](#included-helper-classes)
- [SASS file structure](#sass-file-structure)
- [Grid](#grid)
- [JS](#js)
- [Included JS files](#included-js-files)
- [Included plugins](#included-plugins)

## About

Pippip v3 is a Drupal 8 base theme, utilising Webpack, Browsersync, ES6 & SASS.

#### Browser support

- Edge
- Chrome
- FF
- Safari

## Setup

- Place all provided image assets in `./assets/img`
- Place all fonts in `./dist/fonts`
- From the root pippip folder:
  - Run `npm install`
  - Update `localUrl` in `gulpfile.js` with local site domain
  - Run `gulp` to start compiling & watching the files

## Webpack

Pippip v3 runs [Webpack](https://webpack.js.org/). Run `npm i` from the theme folder to install dependencies, then `npm start` to begin development

## CSS

Pippip v3 is [SASS](https://sass-lang.com) based. Folder structure loosely follows the [Patterlab methodology](https://patternlab.io/)

#### Included helper classes

- `.hidden` - forcibly hides element from view & screen readers

#### SASS file structure

- `./assets/sass/global.scss` contains all imports to generate single `dist/css/style.css`
- `./config/*` contains global variables
- `./helpers/*` contains animations, breakpoints & global mixins
- `./base/*` contains CSS normalize, D8 specific, global and typography stylesheets
- `./templates/*` contains template level stylesheets (e.g. CT level)
- `./organisms/*` contains organism level stylesheets (e.g. header, footer)
- `./molecules/*` contains molecule level stylesheets (e.g. entities, nav)
- `./atoms/*` contains atom level stylesheets (e.g. buttons)

#### Grid

Pippip utilises [Reflex grid](http://reflexgrid.com/docs/) for grid layouts. Reflex grid is a lightweight flexbox based mobile-first grid system.

See [documentation](http://reflexgrid.com/docs/) for details & usage.

## JS

Pippip v3 is ES6 based (rather than jQuery) by default, and gets converted to ES5 on compile for better browser support.

#### Included JS files

- `assets/js/defaults.js` contains all the default plugins & global functions
- `assets/js/global.js` is a blank file for global project specific JS
- `assets/js/emmsg.js` contains emergency message js

#### Included plugins

Usage notes for each plugin can be found in `assets/js/defaults.js`

- [BaugetteBox](https://www.npmjs.com/package/baguettebox.js)
  - Image lightbox
- [Choices](https://www.npmjs.com/package/choices.js)
  - Better select elements
- [Flickity](https://www.npmjs.com/package/flickity)
  - Carousels
  - **Disabled by default** See notes in `./assets/js/defaults.js` for enabling
- [Zenscroll](https://github.com/zengabor/zenscroll)
  - Anchor scroll animation
- [VanillaModal](https://www.npmjs.com/package/vanilla-modal)
  - Custom modal overlays
- [Van11y accessible accordion](https://github.com/nico3333fr/van11y-accessible-accordion-aria)
  - Accessible vanilla JS accordion
