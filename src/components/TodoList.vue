<template>
  <div class="todoList">
    <h1>{{ title }}</h1>
    <search></search>
    <sort></sort>
    <list :todos="todos"></list>
  </div>
</template>

<script>
  import Search from './Search'
  import Sort from './Sort'
  import List from './List'

  export default {
    name: 'todoList',
    components: {
      Search,
      Sort,
      List
    },
    data () {
      return {
        title: 'TodoListTodoListTodoList',
        todos: [
          {text: "asdasd"},
          {text: "qewhkqjehkqjweh"},
          {text: "znncvj"},
          {text: "1132234234"},
          {text: "sdgj"}
        ]
      }
    }
  }
</script>

<style scoped>
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
