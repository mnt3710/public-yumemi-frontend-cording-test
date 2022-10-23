<template>
  <div>
    <Header />
    <Body />
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import Body from '../organisms/Body.vue'

export default Vue.extend({
  components: { Body },
})
</script>
