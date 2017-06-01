<template>
  <div class="list">
    <ul>
      <li v-for="todo in filteredTodos">
        <detail :todo="todo"></detail>
      </li>
    </ul>
  </div>
</template>

<script>
  import Detail from './Detail.vue'

  export default {
    name: 'list',
    props: ['todos', 'filterOptions'],
    components:{
      Detail
    },
    data () {
      return {}
    },
    computed: {
      filteredTodos() {
        return this.todos.filter(v=>{
          if(this.filterOptions.important.includes("모두")) return true;
          return this.filterOptions.important.includes(v.important);
        }).filter(v=>{
          if(this.filterOptions.comp.includes("모두")) return true;
          return this.filterOptions.comp.includes(v.comp ? "완료" : "미완료");
        });
      }
    }
  }
</script>

<style scoped></style>
