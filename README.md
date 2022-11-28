# WorkAdventure Map Starter Kit

![map](./map.png)

This is a starter kit to help you build your own map for [WorkAdventure](https://workadventu.re).

To understand how to use this starter kit, follow the tutorial at [https://workadventu.re/map-building](https://workadventu.re/map-building).

## Structure
* **tilesets** : All tilesets
* **public** : Static files
* **src** : All TypeScript/Javascript scripts
* **map.[json|tmj]** : Map file
* **map.png** : Image displayed on README.md and on the map infos in-game

If you want to use more than one map file, just add the new map file in the root folder, your tilesets in the assets folder and a new script if you need it in the src folder (it will be automaticaly optimized in production).

If you are going to create custom websites to embed in the map, please reference the HTML files in the `input` option in *vite.config.js*.

## Requirements

Node.js version >=16

## Installation

With npm installed (comes with [node](https://nodejs.org/en/)), run the following commands into a terminal in the root directory of this project:

```shell
npm install
npm run dev
```

## Test optimized map
You can test the optimized map as you do in production:
```sh
npm run build
npm run preview
```

## Test your scripts
You can create unit tests for your scripts, you have just to create a [Mocha](https://mochajs.org) test file inside `tests/unit` folder, name your file like this `mytest.test.[ts|js]` and run the following command :
```sh
npm run test
```

## Test your map with scenarios
You can create e2e tests with customs scenarios, create a [PlayWright](https://playwright.dev) test file inside `tests/e2e` folder, name your file like this `mytest.spec.[ts|js]` and run the following command :
```sh
npm run e2e
```

Or this command if you want to see tests inside browsers:
```sh
npm run e2e-headed
```

## Licenses

This project contains multiple licenses as follows:

* [Code license](./LICENSE.code) *(all files except those for other licenses)*
* [Map license](./LICENSE.map) *(`map.[json|tmj]` and the map visual as well)*
* [Assets license](./LICENSE.assets) *(the files inside the `src/assets/` folder)*

### About third party assets

If you add third party assets in your map, do not forget to:
1. Credit the author and license with the "tilesetCopyright" property present in the properties of each tilesets in the `map.[json|tmj]` file
2. Add the license text in LICENSE.assets
