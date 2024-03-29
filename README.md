# svelte material

This is a collection of Material Design components for [Svelte](https://svelte.technology).

It is based on [Material Components Web](https://material-components.github.io/material-components-web-catalog/#/).

The components are located in the /mdc folder.
Their templates are located in the /mdc-templates folder.

The templates, although optional, are useful if components need to be quickly implemented on some projects. They add that extra layer of abstraction.

This app is an example of how to combine multiple components together.
The collection makes it easy to create a material app with Svelte!

---

To create a new project based on this template using [degit](https://github.com/Rich-Harris/degit):

```bash
npm install -g degit # you only need to do this once

degit sveltejs/template svelte-app
cd svelte-app
```

_Note that you will need to have [Node.js](https://nodejs.org) installed._

## Get started

Install the dependencies...

```bash
cd svelte-app
npm install
```

...then start [Rollup](https://rollupjs.org):

```bash
npm run dev
```

Navigate to [localhost:5000](http://localhost:5000). You should see your app running. Edit a component file in `src`, save it, and reload the page to see your changes.

## Deploying to the web

### With [now](https://zeit.co/now)

Install `now` if you haven't already:

```bash
npm install -g now
```

Then, from within your project folder:

```bash
now
```

As an alternative, use the [Now desktop client](https://zeit.co/download) and simply drag the unzipped project folder to the taskbar icon.

### With [surge](https://surge.sh/)

Install `surge` if you haven't already:

```bash
npm install -g surge
```

Then, from within your project folder:

```bash
npm run build
surge public
```
