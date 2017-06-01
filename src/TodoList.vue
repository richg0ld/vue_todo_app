<template>

  <div class="todoList">
    <header>
      <h1 class="todoList__title"><img src="./assets/logo.png" height="50" width="50" :title="title"/></h1>
      <add :addTodo="addTodo"></add>
    </header>

    <content>
      <sort :filterOptions="filterOptions"></sort>
      <list :todos="todos"
            :filterOptions="filterOptions"
      ></list>
    </content>
  </div>
</template>

<script>
  import Add from './components/Add'
  import Sort from './components/Sort'
  import List from './components/List'

  export default {
    name: 'todoList',
    components: {
      Add,
      Sort,
      List
    },
    data () {
      return {
        title: 'TodoListTodoListTodoList',
        filterOptions: {
          important: ["모두"],
          comp: ["모두"]
        },
        todos: [
          {
            "comp":true,
            "important": "중요",
            "date": "2016.12.15",
            "text": "테스트용 데이터 입니다. 확인해주셔서 감사합니다."
          }, {
            "comp":false,
            "important": "매우중요",
            "date": "2016.12.15",
            "text": "Blah, Blah."
          }
        ]
      }
    },
    methods: {
      addTodo (todo) {
        this.todos.push(todo);
      }
    }
  }
</script>

<style scoped>
  header {
    border-bottom:1px solid rgba(0,0,0,0.25);
  }
  .todoList__title {
    width:70px;
    height:70px;
    text-align: center;
    vertical-align: center;
  }
</style>
