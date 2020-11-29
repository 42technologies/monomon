monomon
===========

A tiny wrapper around [nodemon](https://github.com/remy/nodemon) that will automatically
watch all your linked `node_module`s while ignoring all the rest. As the name says,
it should solve your `nodemon` problems when you use a lot linked modules, such as when
having monorepos ([Lerna](https://github.com/lerna/lerna), Yarn Workspaces, etc.).

## Usage

Use the script as you would normally use `nodemon`. Behind the scenes the script will add any
linked module in the `./node_modules` directory to the watchlist. For example:

```
monomon -V server.js
```

## Arguments

The following arguments  are used directly by `monomon` and therefore will not be forwarded to `nodemon`.

### --ignorePackage

Excludes a specific linked package from the watchlist

```
monomon --ignorePackage myLinkedPackage1 --ignorePackage myLinkedPackage2 server.js
```
