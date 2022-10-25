<template>
  <div class="index-molecules-check-boxes">
    <div v-for="value of prefList" :key="value">
      <CheckBox :boxText="value.prefName" />
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
  padding: 5px 10px;
}
</style>
