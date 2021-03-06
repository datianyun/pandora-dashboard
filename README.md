# Pandora Dashboard

A local Dashboard for the Pandora.js. 

The Dashboard it is a standard Pandora.js Project, manage it like a normal Project.

## Usage

### Install globaly

```bash
$ npm i pandora-dashboard -g # install pandora-dashboard globally
$ pandora start --name dashboard `pandora-dashboard-dir` # start it
```

open `http://127.0.0.1:9081`

## Custom TCP Port and IP Address

By default, The Dashboard listens to `http://127.0.0.1:9081`. But it also can tell The Dashboard a specific TCP Port and a specific IP Address to listen on.

```bash
pandora start --name dashboard --env "DASHBOARD_PORT=9081 DASHBOARD_HOST=0.0.0.0" `pandora-dashboard-dir`
```

## HTTP Auth

Set a environment variable like below:

```bash
pandora start --name dashboard --env "DASHBOARD_AUTH=admin:admin" `pandora-dashboard-dir`

```

## How to Contribute

### Back-End

Run `pandora dev`, that will start the project by TypeScript source files through `ts-node/register`.
### Front-End

The front-end is a React application which relies on `[react-router](https://github.com/ReactTraining/react-router)` for navigation. `[webpack](https://github.com/webpack/webpack)` is being used as the module resolver and the build tool producing a single `bundle.js` for distribution.

**webpack-dev-server**

1. Run `npm run dev-public`, that will start a `webpack-dev-server` to listens on default port `8080`.
2. Run `pandora dev --env="DASHBOARD_PUBLIC_BASE_URL=http://localhost:8080/public/build"` to tell back-end use `webpack-dev-server` as the bundle URL.

**build**

The source files in the folder `./public/src`, you can run `npm run build-public` to build it into `./public/build`.
