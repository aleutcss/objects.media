# Media

The Media object module is aleutcss’ implementation of [Nicole
Sullivan](https://twitter.com/stubbornella)’s <cite>media object</cite>—the
poster child of OOCSS.

To find out where it all started, read [Nicole’s blog
post](http://www.stubbornella.org/content/2010/06/25/the-media-object-saves-hundreds-of-lines-of-code/).

## Dependencies

aleutcss’ Media object depends on three other aleutcss modules:

* [settings.defaults](https://github.com/aleutcss/settings.defaults)
* [tools.functions](https://github.com/aleutcss/tools.functions)
* [trumps.clearfix](https://github.com/aleutcss/trumps.clearfix)

If you install the Media object using NPM, you will get these dependencies at
the same time. If not using NPM, please be sure to install and `@import` these
dependencies in the relevant way.

## Installation

The recommended installation method is NPM, but you can install the Media
module via a Git Submodule, or copy and paste.

### 

### Install using npm:

    $ npm install --save-dev aleut-media

Once installed, `@import` into your project in its Objects layer:

    @import "node_modules/inuit-media/objects.media";

### Install as a Git Submodule

    $ git submodule add git@github.com:aleutcss/objects.media.git

Once installed, `@import` into your project in its Objects layer:

    @import "objects.media/objects.media";

### Install via file download

The least recommended option for installation is to simply download
`_objects.media.scss` into your project and `@import` it into your project in
its Objects layer.

## Usage

Basic usage of the Media object uses the required classes:

    <div class="o-media">
        <img src="/path/to/image.png" alt="" class="o-media__img" />
        <div class="o-media__body">
            <p>Text-like content goes here.</p>
        </div>
    </div>

The only valid children of the `.o-media` node are `.o-media__img` and
`.o-media__body`.

## Options

Other, optional classes can supplement the required base classes:

* `.o-media--flush`: remove the space between the image- and text-content.
* `.o-media--[tiny|small|large|huge]`: alter the spacing between the image- and
  text-content.
* `.o-media--rev`: reverse the horizontal rendered order of the image- and
  text-content.
* `.o-media--responsive`: a very basic responsive implementation of the media
  object. Pragmatic; far from perfect.

For example:

    <div class="o-media  o-media--flush  o-media--rev">
        <img src="/path/to/image.png" alt="" class="o-media__img" />
        <div class="o-media__body">
            <p>Text-like content goes here.</p>
        </div>
    </div>
