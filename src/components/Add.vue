<template>
  <section class="add">
    <label for="add_important" v-show="false">중요도 선택</label>
    <select name="important" id="add_important" class="search__select--important" v-model="important">
      <option value="">중요도</option>
      <option value="매우중요">매우중요</option>
      <option value="중요">중요</option>
      <option value="보통">보통</option>
    </select>
    <div class="search__input--todo-wrap">
      <input type="text" name="todo" class="search__input--todo" placeholder="할 일을 입력하세요." v-model="text" @keyup.enter="addNewTodo" />
    </div>
    <button type="button" class="search__button--add-todo" @click="addNewTodo" >추가</button>
  </section>
</template>

<script>
  export default {
    name: 'add',
    props:["addTodo"],
    data () {
      return {
        important: "",
        text:""
      }
    },
    methods: {
      addNewTodo () {
        if (!this.important || !this.text) return;
        const d = new Date();
        this.addTodo({
          comp:false,
          important: this.important,
          date: `${d.getFullYear()}.${d.getMonth()+1}.${d.getDate()}`,
          text: this.text,
        });
        this.important = "";
        this.text = "";
      }
    }
  }
</script>

<style scoped></style>
