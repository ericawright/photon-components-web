# photon-components-web

[![CircleCI](https://circleci.com/gh/FirefoxUX/photon-components-web.svg?style=svg)](https://circleci.com/gh/FirefoxUX/photon-components-web)

This repository contains CSS styles and some React components to replicate the standard styles used in Firefox. The most recent style guidelines for Firefox are called "Photon" (hence the name of this repository).

These components are intended to be used anywhere where you want to make an HTML interface appear to be part of the browser itself. Examples where this might be useful include add-ons/extensions, UI directly in Firefox that is implemented in HTML, and some Mozilla properties like addons.mozilla.org.

This repository is not intended for a general audience. You do not have to use React to make use of the styles.

## Preview & Download

Preview the latest build from master here:
* <https://firefoxux.github.io/photon-components-web/>

Download the latest build from master here:
* <https://firefoxux.github.io/photon-components-web/dist.zip>

## Development

To get started:

```sh
npm install
# To generate static CSS and images/ in dist/ :
npm run build:webpack
# To generate a static Storybook in storybook/ :
npm run build:storybook
# To run the demonstration site locally on http://localhost:9001/ :
npm start
```

## Conventions

Components are styled using the [BEM](http://getbem.com/) (Block-Element-Modifier) convention:

* Top-level components are "blocks"
  * e.g. `button`
* Parts of components are "elements", and are namespaced by their block:
  * e.g. `card__media` as a sub-element of `card`
* `modifiers` are optional or stateful properties applied to the markup:
  * Top-level modifiers are namespaced to their block, e.g. `button--primary`
  * Element-level modifiers namespace to their element, e.g. `card__media--loading`
  
In general this code should try to conform to [Firefox CSS Guidelines](https://developer.mozilla.org/en-US/docs/Mozilla/Developer_guide/CSS_Guidelines) and when possible the [Firefox Devtools CSS Guidelines](https://docs.firefox-dev.tools/contributing/css.html).
