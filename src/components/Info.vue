<template>
  <div class="info">
    <dl class="info__todo-data--comp-date">
      <dt>중요도 :</dt><dd>{{ todo.important }}</dd><br/>
      <dt>추가일 :</dt><dd>{{ todo.date }}</dd>
    </dl>
    <p class="info__todo-data--todo" @dblclick="editTodo(todo)">{{ todo.text }}</p>
  </div>
</template>
<script>
  export default {
    name: 'info',
    props: ['todo', 'editTodo'],
    data () {
      return {}
    }
  }
</script>

<style scoped></style>
