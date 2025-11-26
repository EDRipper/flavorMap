# Map Editing Starter Kit

![office map thumbnail](https://hc-cdn.hel1.your-objectstorage.com/s/v3/ce6bbeda3d0d9f68e2fb4782877c955aab87580b_image.png)

This codebase can host maps (including assets, bounding boxes and event triggers + scripts) for development, providing a playable link which can be uploaded to the main flavor town instance.

Flavor Town / Work Adventure loads the map from a URL, in our case, https://hackclub.github.io/flavorMap/ (hosted with github pages. Changes to the Repo are automatically applied) 

The map is in 32*32px, I recommend editing with the Tiled editor, as it handles tmj files well.

Work Adventure has good guidance on this: [https://docs.workadventu.re/map-building/tiled-editor/](https://docs.workadventu.re/map-building/tiled-editor/).

For issues, questions or suggestions, DM me @EuanRipper on slack. (Don't tell me i pushed the .env, it is non sensitive!)

## How to Make your own house / edit a map

Clone this repo and open the office.tmj file in Tiled (make sure it is within this repo, not an isolated file.)

When adding in any external assets, be sure to add them to the public images in this repo and embedd the tileset into the map, **this is important**.

All basic map editing skills are well documented in [youtube tutorials:](https://www.youtube.com/watch?v=lu1IZgBJJD4&list=PL7jmrMKZfjCnz36FvezxJ-Tshuh3Zz-nc)

Always follow this file structure:

* *public/*: Static files like PDFs or audio files
* *src/*: Scripts files or design source files
* *tilesets/*: All PNG tilesets


Publish your fork on github and host with github pages.

Message Euan Ripper to get your map linked in to the main flavor Town instance.

## Contribution Guidelines

-If you make a change that invalidates information in this README, update this README. 

-PRs welcome, just be a good egg.

> **Pro tips**
> If you want to use more than one map file, just add the new map file in the root folder (I recommend creating a copy of *office.tmj* and editing it, in order to avoid any mistakes).  
> use 512x512 images for the map thumbnails.
> If you are going to create custom websites to embed in the map, please reference the HTML files in the `input` option in *vite.config.js*.

## Requirements

Node.js version >=17

## Installation and testing

With npm installed (comes with [node](https://nodejs.org/en/)), run the following commands into a terminal in the root directory of the project:

```shell
npm install
```

Then, you can test your map by running:

```sh
npm run dev
```

You can also test the optimized map as it will be in production by running:

```sh
npm run build
npm run prod
```

You can manually upload your map to the map storage by running:

```sh
npm run deploy
```

## Licenses 
Do not violate the license agreements of WorkAdventure:


* [Code license](./LICENSE.code) *(all files except those for other licenses)*
* [Map license](./LICENSE.map) *(`office.tmj` and the map visual as well)*
* [Assets license](./LICENSE.assets) *(the files inside the `src/assets/` folder)*

### About third party assets

If you add third party assets in your map, do not forget to:

1. Credit the author and license of a tileset with the "tilesetCopyright" property by etiding the tileset in Tiled.
2. Add the tileset license text in *LICENSE.assets*.
3. Credit the author and license of a map with the "mapCopyright" property in the custom properties of the map.
4. Add the map license text in *LICENSE.map*.
