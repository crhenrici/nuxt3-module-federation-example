# Nuxt 3 Module Federation example

| :exclamation:  Module Federation does not work on client. It is the purpose of this repository to get it working.   |
|-----------------------------------------|

This repository showcases how to use Nuxt 3 with Module Federation. It is also used as a reproduction for `shared module not available for eager consumption: Vue` bug.

## Getting started
The repository is structured as a Lerna monorepo, where `nuxt3-app` package is for the Nuxt 3 host and `remote` package is for Vue CLI-generated component remote.

In order to get started, you will need Lerna. You can also get it from `devDependecies`:
```cmd
npm i
```

You can quickly install all the package dependencies using
```cmd
npx lerna bootstrap
```

## Building
In order to build the packages, simply run
```cmd
npm run build
```
When run on project root, it will build all the packages. When run in `packages/*`, it will build the individual packages.

## Starting
To start the Nuxt host and Vue remote, use
```cmd
npm start
```

As with the build command, you can run it either on project root or on individual package root.

## Exposed applications

Nuxt is exposed at http://localhost:3000.

Vue remote is exposed at http://localhost:3101.

You can navigate to http://localhost:3101/client to see the host version of Vue remote.

## Troubleshooting

Please, note that you need to have at least Node.js 14 or 16 and npm version 7.

As Nuxt is currently in beta, the project may unexpectedly break. In that case, try locking its version to 3.0.0-27252573.ad7e755 (modify `packages/nuxt3-app/package.json` by removing ^ in `nuxt3` and reinstalling dependencies). The mentioned version is guaranteed to run.

If you still cannot get the project running, [file an issue](https://github.com/phoenix-ru/nuxt3-module-federation-example/issues/new) in case you encounter.