<template>
  <section class="sort">
    <div class="sort--important">
      <span class="sort__checkbox--important">
          <input id="f_i_0" type="checkbox" name="important" />
          <label for="f_i_0">모두</label>
      </span>
      <span class="sort__checkbox--important">
          <input id="f_i_1" type="checkbox" name="important" />
          <label for="f_i_1">매우중요</label>
      </span>
      <span class="sort__checkbox--important">
          <input id="f_i_2" type="checkbox" name="important" />
          <label for="f_i_2">중요</label>
      </span>
      <span class="sort__checkbox--important">
          <input id="f_i_3" type="checkbox" name="important" />
          <label for="f_i_3">보통</label>
      </span>
    </div>
    <div class="sort--complete">
      <span class="sort__checkbox--complete">
          <input id="f_c_0" type="checkbox" name="comp" />
          <label for="f_c_0">모두</label>
      </span>
      <span class="sort__checkbox--complete">
          <input id="f_c_1" type="checkbox" name="comp" />
          <label for="f_c_1">완료</label>
      </span>
      <span class="sort__checkbox--complete">
          <input id="f_c_2" type="checkbox" name="comp" />
          <label for="f_c_2">미완료</label>
      </span>
    </div>
  </section>
</template>

<script>
  export default {
    name: 'sort',
    data () {
      return { }
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
