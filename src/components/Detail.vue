<template>
  <div class="detail">
    <input class="detail__checkbox--comp" type="checkbox" name="comp" v-model="todo.comp" />
    <info v-if="!isEditing"
          :todo="todo"
          :editTodo="editTodo"
    ></info>
    <modify v-else
            :todo="todo"
            :doneEditTodo="doneEditTodo"
            :cancelEditTodo="cancelEditTodo"
    ></modify>
  </div>
</template>
<script>
  import Info from './Info.vue'
  import Modify from './Modify.vue'

  export default {
    name: 'detail',
    props: ['todo'],
    components:{
      Info,
      Modify
    },
    data () {
      return {
        isEditing:false,
        beforeEditCache: {
          important:"",
          text:""
        }
      }
    },
    methods:{
      editTodo () {
        this.isEditing = true;
        this.beforeEditCache.important=this.todo.important;
        this.beforeEditCache.text=this.todo.text;
        console.log("에디트!");
      },
      doneEditTodo () {
        this.isEditing = false;
        this.beforeEditCache.important="";
        this.beforeEditCache.text="";
        console.log("에디트 완료!");
      },
      cancelEditTodo () {
        this.isEditing = false;
        this.todo.important = this.beforeEditCache.important;
        this.todo.text = this.beforeEditCache.text;
        console.log("취소!");
      }
    }
  }
</script>

<style scoped></style>
