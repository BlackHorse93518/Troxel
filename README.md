Troxel [![Travis Build Status (Linux)](https://travis-ci.org/chrmoritz/Troxel.svg?branch=master)](https://travis-ci.org/chrmoritz/Troxel) [![AppVeyor Build status (Windows)](https://ci.appveyor.com/api/projects/status/glwcnbd0k2qh6f29/branch/master?svg=true)](https://ci.appveyor.com/project/chrmoritz/troxel/branch/master) [![Code Climate](https://codeclimate.com/github/chrmoritz/Troxel/badges/gpa.svg)](https://codeclimate.com/github/chrmoritz/Troxel)  [![devDependency Status](https://david-dm.org/chrmoritz/Troxel/dev-status.svg)](https://david-dm.org/chrmoritz/Troxel#info=devDependencies) [![Codacy Badge](https://api.codacy.com/project/badge/grade/03e55ccb36d94a9eab093851d8b3ca99)](https://www.codacy.com/app/chrmoritz/Troxel) [![JS.ORG](https://img.shields.io/badge/js.org-troxel-brightgreen.svg?style=flat)](https://js.org/)
======

Troxel is a WebGL-based HTML5-WebApp for viewing and editing voxel models with some additional support for [Trove](http://www.trionworlds.com/trove/) specific features.  Visit [troxel.js.org](https://troxel.js.org/) to try it out! You can embed Troxel in your own website too with [libTroxel](#libtroxel).

## Features ##
* Supported file formats for both import and export
  * Qubicle (.qb): fully supported (multi matrix, compression ...)
  * Magica Voxel (.vox)
  * Zoxel (.zox)
  * Base64 (links): Troxel's own compressed file format for sharing models via links
  * JSON: raw data output
  * some additions for material maps (multi-layer voxel data) used by Trove
* WebGL-based 3D-Renderer
  * basic support for all material maps
* Editor
  * simple add and remove voxel functionality
  * rotate, mirror, move and resize voxel model
  * filltool with color noise

## How to use
#### Dependencies:
* [Node.js](https://nodejs.org/) 4+
* for hosting static page locally (optionally): [ruby](https://www.ruby-lang.org/) with github-pages gem (`gem install github-pages`)

#### Installing
```
git clone git@github.com:chrmoritz/Troxel.git
cd troxel
npm install
```
#### Running dev server
```
npm start
```
Then open: http://localhost:3000/index.jade

*This server will automatically recompile resources after editing them. You only need to reload you page to see your edits live.*

#### Running tests
```
npm test
```
*Please run this test suite before opening a pull request.*

#### Building a static page
```
npm run build
```
*The static page will be generated into the `dist` folder.*

#### Serving the static page via jekyll
```
npm run serve
```
*The static page will be served by Jekyll (like on GitHub Pages) and grunt will watch for source file changes and automatically recompile these changes and update Jekyll.*

**Note:** *You need the github-pages gem installed (`gem install github-pages`) for this.*

#### Importing Trove's blueprints
Check out [troxeljs/trove-blueprints](https://github.com/troxeljs/trove-blueprints) for more information about how to import blueprints.

libTroxel
======

[LibTroxel](https://github.com/troxeljs/libtroxel) is a JavaScript library which allows you to embedd voxel models rendered with Troxel into your own website. The project lives now in its own subproject at [troxeljs/libtroxel](https://github.com/troxeljs/libtroxel).
