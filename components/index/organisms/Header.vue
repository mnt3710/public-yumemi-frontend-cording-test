<template>
  <div class="index-organisms-header">
    <HeaderTitle />
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import HeaderTitle from '../atoms/HeaderTitle.vue'

export default Vue.extend({
  components: { HeaderTitle },
})
</script>

<style scoped>
.index-organisms-header {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 5vh;
  background-color: #3856ff8f;
}
</style>
