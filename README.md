# 🌺 Frisque StoryBlok

> Welcome to the Frisque StoryBlok starter kit! This is currently a WIP project that aims to simplify the setup of connecting NuxtJS to StoryBlok. It also aims to provide an opinionated framework and directory structure to get you going immediately.
>
> This project contains a few default configurations out of the box such as TailwindCSS, Linting (ESLint, StyleLint, Prettier, CommitLint), Testing suite using JEST, and some NPM scripts to make development a breeze.
>
> Some key directories and files to take a look at would be the `/components` directory as well as the `/pages/_.vue` file. The latter sets up the view and loads the proper components from the `/components` directory.

## 📓 Table of contents

- [System Requirements](#✅-system-requirements)
- [Build Setup](#💻-build-setup)
- [Special Directories](#📂-special-directories)
- [Resources](#📚-resources)

## ✅ System Requirements

- Unix-like OS (windows support is limited atm)
- Node Version >= 16.13.2
- NPM Version >= 8.1.2

## 💻 Build Setup

To get started create a `.env` file in the root of this project with the following information

```dotenv
STORYBLOK_ACCESS_TOKEN="Your Access Token Here"
```

For more information on how to create your StoryBlok Access Token [click here](https://www.storyblok.com/faq/where-to-find-my-content-delivery-api-key).

```bash
# install dependencies
$ npm install

# serve with hot reload at localhost:3000
$ npm run dev

# build for production and launch server
$ npm run build
$ npm run start

# generate static project
$ npm run generate

# create a StoryBlok component
$ npm run create-component

# Run Linters (ESLint, StyleLint, PrettierLint)
$ npm run lint
$ npm run lint:js
$ npm run lint:style
$ npm run lint:prettier

# Run the Lint Fixer
$ npm run lintfix

# Prepare the githooks
$ npm run prepare
```

## 📂 Special Directories

You can create the following extra directories, some of which have special behaviors. Only `pages` is required; you can delete them if you don't want to use their functionality.

### `📁 assets`

The assets directory contains your uncompiled assets such as Stylus or Sass files, images, or fonts.

More information about the usage of this directory in [the documentation](https://nuxtjs.org/docs/2.x/directory-structure/assets).

### `📁 components`

The components directory contains your Vue.js components. Components make up the different parts of your page and can be reused and imported into your pages, layouts and even other components.

More information about the usage of this directory in [the documentation](https://nuxtjs.org/docs/2.x/directory-structure/components).

### `📁 layouts`

Layouts are a great help when you want to change the look and feel of your Nuxt app, whether you want to include a sidebar or have distinct layouts for mobile and desktop.

More information about the usage of this directory in [the documentation](https://nuxtjs.org/docs/2.x/directory-structure/layouts).

### `📁 pages`

This directory contains your application views and routes. Nuxt will read all the `*.vue` files inside this directory and setup Vue Router automatically.

More information about the usage of this directory in [the documentation](https://nuxtjs.org/docs/2.x/get-started/routing).

### `📁 plugins`

The plugins directory contains JavaScript plugins that you want to run before instantiating the root Vue.js Application. This is the place to add Vue plugins and to inject functions or constants. Every time you need to use `Vue.use()`, you should create a file in `plugins/` and add its path to plugins in `nuxt.config.js`.

More information about the usage of this directory in [the documentation](https://nuxtjs.org/docs/2.x/directory-structure/plugins).

### `📁 static`

This directory contains your static files. Each file inside this directory is mapped to `/`.

Example: `/static/robots.txt` is mapped as `/robots.txt`.

More information about the usage of this directory in [the documentation](https://nuxtjs.org/docs/2.x/directory-structure/static).

### `📁 store`

This directory contains your Vuex store files. Creating a file in this directory automatically activates Vuex.

More information about the usage of this directory in [the documentation](https://nuxtjs.org/docs/2.x/directory-structure/store).

## 📚 Resources

### StoryBlok

To learn how to develop with StoryBlok and NuxtJS follow the resources below to get started.

- [StoryBlok Documentation](https://www.storyblok.com/docs)
- [NuxtJS integration with StoryBlok](https://www.storyblok.com/tc/nuxtjs)

### NuxtJS

NuxtJS is an innovative Vue Framework packaged with plenty of features to boost developer productivity and the end user experience.

- [Getting Started with Nuxt](https://nuxtjs.org/docs/get-started/installation)
