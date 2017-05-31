<template>
  <div class="list">
    <ul>
      <li v-for="todo in todos"><a href="https://vuejs.org" target="_blank">{{ todo.text }}</a></li>
    </ul>
  </div>
</template>

<script>
  export default {
    name: 'list',
    props: ['todos'],
    data () {
      return {}
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
