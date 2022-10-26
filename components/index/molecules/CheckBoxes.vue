<template>
  <div class="index-molecules-check-boxes">
    <div v-for="value of prefList" :key="value.prefCode">
      <CheckBox :boxText="value.prefName" @onChecked="addCheckedList" />
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import CheckBox from '../atoms/CheckBox.vue'

export default Vue.extend({
  components: { CheckBox },
  props: {
    prefList: {
      default: '',
      type: Array,
    },
  },
})
</script>

<style scoped>
.index-molecules-check-boxes {
  display: flex;
  flex-wrap: wrap;
  margin: 5px 20px;
  outline-style: solid;
}
</style>
