# nuxt-test

## Build Setup

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
```

For detailed explanation on how things work, check out [Nuxt.js docs](https://nuxtjs.org).

## installing SASS

```bash
# add dependencies
$ npm install --save-dev node-sass sass-loader

# add plugin
$ npm install --save-dev @nuxtjs/style-resources

# create scss folder
Add scss-folder in assets and add scss file

# modify nuxt.config.js

export default {
    //...
    css: [
    '~assets/scss/colors.scss'
  ],
    //...
    modules: [
    '@nuxtjs/style-resources'
  ],

    //You will have to add this new object if it doesn't exist already
  styleResources: {
    scss: ['./assets/scss/*.scss']
  },
    //...
}

```
