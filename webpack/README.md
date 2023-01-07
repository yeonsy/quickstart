# Webpack

1. `yarn add --dev webpack webpack-cli`
2. create `webpack.config.js`
3. `yarn webpack`

## webpack.config.js

At a minimum, you will need an entrypoint and output

```js
const path = require('path')

module.exports = {
  entry: './src/index.js',
  output: {
    filename: 'bundle.js',
    path: path.resolve(__dirname, 'dist'),
  },
}
```

