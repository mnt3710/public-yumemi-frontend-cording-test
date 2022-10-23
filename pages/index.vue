<template>
  <div class="index-pages">
    <indexTemplates />
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import indexTemplates from '../components/index/templates/index.vue'

export default Vue.extend({
  components: { indexTemplates },
})
</script>
