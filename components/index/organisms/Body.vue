<template>
  <div class="index-organisms-body">
    <BodyTitle />
    <CheckBoxes :prefList="prefList" />
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import BodyTitle from '../atoms/BodyTitle.vue'
import CheckBoxes from '../molecules/CheckBoxes.vue'

export default Vue.extend({
  components: {
    BodyTitle,
    CheckBoxes,
  },
  props: {
    prefList: {
      default: [],
      type: Array,
    },
  },
})
</script>
