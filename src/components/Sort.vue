<template>
  <section class="sort">
    <div class="sort--important">
      <span v-for="(importantOption, i) in importantOptions" class="sort__checkbox--important">
          <input :id="'fi_'+i" type="checkbox" name="important" :title="importantOption" :value="importantOption" v-model="filterOptions.important"/>
          <label :for="'fi_'+i">{{ importantOption }}</label>
      </span>
    </div>
    <div class="sort--complete">
      <span v-for="(completeOption, i) in completeOptions" class="sort__checkbox--complete">
          <input :id="'fc_'+i" type="checkbox" name="comp" :title="completeOption" :value="completeOption" v-model="filterOptions.comp"/>
          <label :for="'fc_'+i">{{ completeOption }}</label>
      </span>
    </div>
  </section>
</template>

<script>

  export default {
    name: 'sort',
    props: ['filterOptions'],
    data () {
      return {
        importantOptions: ["모두", "매우중요", "중요", "보통"],
        completeOptions: ["모두", "완료", "미완료"]
      }
    }
  }
</script>

<style scoped></style>
