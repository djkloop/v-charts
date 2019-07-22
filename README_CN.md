<p align="center">
<img src="./examples/favicon.ico" alt="mark text" width="100" height="100">
</p>

<h3 align="center">v-charts-multiple-y</h3>

<p align="center">
  <a href="https://travis-ci.org/ElemeFE/v-charts">
    <img src="https://travis-ci.org/ElemeFE/v-charts.svg?branch=master" alt="Build Status">
  </a>
  <a href="https://npmjs.org/package/v-charts">
    <img src="http://img.shields.io/npm/dm/v-charts.svg" alt="NPM downloads">
  </a>
  <a href="https://www.npmjs.org/package/v-charts">
    <img src="https://img.shields.io/npm/v/v-charts.svg" alt="Npm package">
  </a>
  <a>
    <img src="https://img.shields.io/badge/language-javascript-yellow.svg" alt="Language">
  </a>
  <a>
    <img src="https://img.shields.io/badge/license-MIT-000000.svg" alt="License">
  </a>
  <a href="https://gitter.im/ElemeFE/v-charts?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge">
    <img src="https://badges.gitter.im/ElemeFE/v-charts.svg" alt="Join the chat">
  </a>
</p>

<p align="center">
  <a href="https://v-charts.js.org">
    文档
  </a>
  <span> | </span>
  <a href="https://codesandbox.io/s/z69myovqzx">
    示例项目
  </a>
  <span> | </span>
  <a href="https://github.com/djkloop/v-charts/blob/master/README.md">
    English
  </a>
  <span> | </span>
  <a>
    中文
  </a>
</p>

> 基于 Vue2.x 封装的 Echarts 图表组件

# 此魔改库版权归原作者
- 感谢作者提供了这么好的库能在vue中是使用echarts
- 此库仅增加了折线图多Y轴功能（如果不需要建议使用源库）
- 版权还是归属于原作者

## 特性

- **统一的数据格式：** 使用对前后端都友好的数据格式，方便生成和修改。
- **简化的配置项：** 通过简化的配置项，可以轻松实现复杂需求。
- **定制简单：** 提供多种自定义 Echarts 方式，可以方便的设置图表配置项。

## 支持性

支持所有现代浏览器及 IE10+ ，包括 pc 端和移动端。

## 安装

```
npm i v-charts echarts -S
```

## 快速上手

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
        columns: ['date', '年龄', '余额'],
        rows: [
          { 'date': '01-01', '年龄': 1231, '余额': '999', '人数': '578' },
          { 'date': '01-02', '年龄': 1223, '余额': '781', '人数': '1213' },
          { 'date': '01-03', '年龄': 2123, '余额': '321', '人数': '213' },
          { 'date': '01-04', '年龄': 4123, '余额': '654', '人数': '2312' },
          { 'date': '01-05', '年龄': 3123, '余额': '972', '人数': '1233' },
          { 'date': '01-06', '年龄': 7123, '余额': '124', '人数': '2313' }
        ]
      }，
      /*
        yAxisSite
          - site[Array<string>]: 和columns对应
            特殊说明: 数组第一个是左数轴/第二个是右第一个，其他依次排序
          - offset[Array<number>]: 和columns对应
            特殊说明: 数组第一个是左数轴/第二个是右第一个，其他依次排序
        yAxisName 保持和官网一致
      */
      settings: {
        yAxisSite: {
          site: ['年龄', '余额', '人数'],
          offset: [0, 0, 80]
        },
        yAxisName: ['年龄', '余额', '人数']
      }
    }
  }
}
</script>
```

## 更新日志

每个版本的详细修改可以参考 [release notes](https://github.com/ElemeFE/v-charts/releases) 或者 [ChangeLog](./CHANGELOG_CN.md)。

## 贡献

在发起一个 pull request 之前，请先阅读[贡献指南](./CONTRIBUTING_CN.md)。

## License

[MIT](http://opensource.org/licenses/MIT)
