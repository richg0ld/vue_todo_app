<template>
  <section class="search">
    <select name="important" id="important" class="search__select--important">
      <option value="">중요도</option>
      <option value="매우중요">매우중요</option>
      <option value="중요">중요</option>
      <option value="보통">보통</option>
    </select>
    <div class="search__input--todo-wrap">
      <input type="text" name="todo" class="search__input--todo" placeholder="할 일을 입력하세요." />
    </div>
    <button type="button" class="search__button--add-todo" >추가(width:80px)</button>
  </section>
</template>

<script>
  export default {
    name: 'search',
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
