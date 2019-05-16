<template>
  <div id="app">
    <h1>Used for Test Components</h1>
    <h2>Young Vue Components</h2>

    <young-pagination
    :totalPage='totalPage'
    :currentPage='currentPage'
    v-on:current-change='currentChange'
    ></young-pagination>
    <p>
      {{msg}}
    </p>
  </div>
</template>
<script>
import youngPagination from './lib/pagination/youngPagination.vue'
export default {
  name: 'app',
  data () {
    return {
      totalPage: 50,
      currentPage: 2,
      msg: ''
    }
  },
  components: {
    youngPagination
  },
  methods: {
    currentChange (val) {
      this.msg = `正在请求第${val}页`
    }
  }
}
</script>

<style scoped>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
