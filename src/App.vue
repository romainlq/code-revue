<template>
  <div id="app">
    <PostIt title="Pull Request de " />
    <PostIt title="Reviewer" />
    <Table :list="list"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import PostIt from './components/Postit.vue'
import reviewList from './data/data.json'
import Table from './components/Table.vue'

export default {
  name: 'app',
  components: {
    HelloWorld,
    PostIt,
    Table
  },
  data: function() {
    return {
      list: [
        {
          id: 1,
          reviewer: reviewList[1],
          reviewed: reviewList[3]
        },
        {
          id: 2,
          reviewer: reviewList[3],
          reviewed: reviewList[0]
        },
        {
          id: 3,
          reviewer: reviewList[0],
          reviewed: reviewList[2]
        },
        {
          id: 4,
          reviewer: reviewList[2],
          reviewed: reviewList[1]
        }
      ]
    }
  }
}
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
