# young-vue-components

> A self-implemented Vue component library

## 支持组件
* pagination

## 安装

`npm install young-vue-components`
## 使用方法
```
<template>
<div>
  <young-pagination
    :totalPage='100'
    :currentPage='1'
  >
  <young-pagination>
</div>
</template>
import {youngPagination} from 'young-vue-components'
export default {
  name: 'app',
  components: {
    youngPagination
  }
}
```
## Props
* totalPage: Number

  总页数，此字段是必须的
* currentPage: Number

  当前页数，此字段默认为1

## Events
* current-change

  访问页面改变时触发，返回要访问的页码
