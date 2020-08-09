# au2buildsetup

This project is bootstrapped by [aurelia/new](https://github.com/aurelia/new).

## Start dev web server

    npm start

## Build the app in production mode

    npm run build

It builds `dist/*-bundle.[hash].js`, updates index.html with hashed js bundle file name. To deploy to production server, copy over both the generated `index.html` and all the `dist/*` files.

For example
```
index.html
dist/entry-bundle.12345.js
```
Copy to production root folder
```
root_folder/index.html
root_folder/dist/entry-bundle.12345.js
```

## Unit Tests

    npm run test

Run unit tests in watch mode.

    npm run test:watch


## Clear tracing cache

In rare situation, you might need to run clear-cache after upgrading to new version of dumber bundler.

    npm run clear-cache

## index.html

`index.html` is generated from `_index.html` every time `npm run build` runs. It is handled by dumber's `onManifest()` option, check `gulpfile.js` for details.

## Cypress e2e test

All e2e tests are in `cypress/integration/`.

Run e2e tests with:

    npm run test:e2e

Note the `test:e2e` script uses start-server-and-test to boot up dev server on port 9000 first, then run cypress test, it will automatically shutdown the dev server after test was finished.

To run Cypress interactively, do

```bash
# Start the dev server in one terminal
npm start
# Start Cypress in another terminal
npx cypress open
```

For more information, visit https://www.cypress.io
