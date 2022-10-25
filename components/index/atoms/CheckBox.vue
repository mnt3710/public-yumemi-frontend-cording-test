<template>
  <div class="index-atoms-check-box">
    <input type="checkbox" />
    <label>{{ boxText }}</label>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  props: {
    boxText: {
      default: '',
      type: String,
    },
  },
})
</script>

<style scoped>
.index-atoms-check-box {
  margin: 10px;
}
</style>
