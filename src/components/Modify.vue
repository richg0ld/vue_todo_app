<template>
  <div class="modify">
    <dl class="modify__todo-data--info">
      <dt><label for="mod_importance">중요도 :</label></dt>
      <dd>
        <select name="importance" id="mod_importance" class="mod__importance" v-model="todo.important">
          <option value="매우중요">매우중요</option>
          <option value="중요">중요</option>
          <option value="보통">보통</option>
        </select>
      </dd>
    </dl>
    <div class="modify__input--wrap">
      <input type="text" name="todo" class="modify__input--todo" placeholder="할 일을 수정하세요." v-model="todo.text"
        @keyup.enter="doneEditTodo"
        @keyup.esc="cancelEditTodo"
      />
      <button type="button" class="modify__button--mod" @click="doneEditTodo">수정</button>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'modify',
    props: ['todo', 'doneEditTodo', 'cancelEditTodo'],
    data () {
      return {}
    }
  }
</script>

<style scoped></style>
