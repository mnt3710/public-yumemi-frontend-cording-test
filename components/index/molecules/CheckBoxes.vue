<template>
  <div>
    <div v-for="i in 10" :key="i.toString()">
      <CheckBox />
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import CheckBox from '../atoms/CheckBox.vue'

export default Vue.extend({
  components: { CheckBox },
})
</script>
