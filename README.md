<p align="center">
<img src="./examples/favicon.ico" alt="mark text" width="100" height="100">
</p>

<h3 align="center">v-charts-multiple-y</h3>

<p align="center">
  <a href="https://npmjs.org/package/v-charts-multiple-y">
    <img src="http://img.shields.io/npm/dm/v-charts-multiple-y.svg" alt="NPM downloads">
  </a>
  <a href="https://www.npmjs.org/package/v-charts-multiple-y">
    <img src="https://img.shields.io/npm/v/v-charts-multiple-y.svg" alt="Npm package">
  </a>
  <a>
    <img src="https://img.shields.io/badge/language-javascript-yellow.svg" alt="Language">
  </a>
  <a>
    <img src="https://img.shields.io/badge/license-MIT-000000.svg" alt="License">
  </a>
</p>

<p align="center">
  <a href="https://v-charts.js.org/#/en/">
    Document
  </a>
  <span> | </span>
  <a href="https://codesandbox.io/s/z69myovqzx">
    Sample Project
  </a>
  <span> | </span>
  <a>
    English
  </a>
  <span> | </span>
  <a href="./README_CN.md">
    中文
  </a>
</p>

> Chart components based on Vue2.x and Echarts

# This magic change library copyright belongs to the original author
- Thanks to the author for providing such a good library to use echarts in vue
- This library only adds a multi-axis function for the line chart (if you do not need to use the source library)
- Copyright still belongs to the original author


## Features
- **Uniform data format:** Use an uniform data format that both convient for frontend and backend, and also easy to create and edit.
- **Simplified configuration:** With simplified configuration items, complex requirements can be easily implemented.
- **Simple customization:** Provide a variety of custom Echarts way, you can easily set the chart options.

## Support

Modern browsers and Internet Explorer 10+, include pc and mobile browser.

## Install

```
npm i v-charts-multiple-y echarts -S
```

## Start

```html
<template>
  <div>
    <ve-line :data="chartData"></ve-line>
  </div>
</template>

<script>
import VeLine from 'v-charts/lib/line.common'
export default {
  components: { VeLine },
  data () {
    return {
      chartData: {
        columns: ['date', 'age', 'balance', 'people'],
        rows: [
          { 'date': '01-01', 'age': 1231, 'balance': '999', 'people': '578' },
          { 'date': '01-02', 'age': 1223, 'balance': '781', 'people': '1213' },
          { 'date': '01-03', 'age': 2123, 'balance': '321', 'people': '213' },
          { 'date': '01-04', 'age': 4123, 'balance': '654', 'people': '2312' },
          { 'date': '01-05', 'age': 3123, 'balance': '972', 'people': '1233' },
          { 'date': '01-06', 'age': 7123, 'balance': '124', 'people': '2313' }
        ]
      }，
      /*
        yAxisSite
          - site[Array<string>]: Corresponds to columns
            Note: The first one of the array is the left number axis / the second one is the right first one, and the others are sorted one by one.
          - offset[Array<number>]: Corresponds to columns
            Note: The first one of the array is the left number axis / the second one is the right first one, and the others are sorted one by one.
        yAxisName Keep consistent with the official website
      */
      settings: {
        yAxisSite: {
          site: ['age', 'balance', 'people'],
          offset: [0, 0, 80]
        },
        yAxisName: ['age', 'balance', 'people']
      }
    }
  }
}
</script>
```

## Changelog

Detailed changes for each release are documented in the [release notes](https://github.com/ElemeFE/v-charts/releases) or [ChangeLog](./CHANGELOG.md).

## Contribution

Please make sure to read the [Contributing Guide](./CONTRIBUTING.md) before making a pull request.

## License

[MIT](http://opensource.org/licenses/MIT)
