# craco-workbox

**Prerequisites**

Install [craco](https://github.com/sharegate/craco)

## Install

```
yarn add craco-workbox -D

# OR

npm install craco-workbox -S
```

## Usage

1. Add the plugin into your craco.config.cjs;

```javascript
// craco.config.js

const CracoWorkboxPlugin = require('craco-workbox');

module.exports = {
    plugins: [{
        plugin: CracoWorkboxPlugin
    }]
}
```

2. Add a workbox.config.js file to your project root containing the overrides you would like to pass. For a full list of options see [https://developers.google.com/web/tools/workbox/modules/workbox-webpack-plugin#generatesw_plugin](https://developers.google.com/web/tools/workbox/modules/workbox-webpack-plugin#generatesw_plugin).

```javascript
// workbox.config.js

module.exports = {
  GenerateSW: options => {
    // override GenerateSW config here
    // e.g. options.skipWaiting = true;
    return options;
  },
  InjectManifest: options => {
    // override InjectManifest config here
    // e.g. options.maximumFileSizeToCacheInBytes = 10 * 1024 * 1024;
    return options;
  }
};
```

## License

Licensed under the MIT License, Copyright ©️ 2019 Kevin S. Perrine. See [LICENSE](LICENSE) for more information.
