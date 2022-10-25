<template>
  <div class="index-template">
    <Header />
    <Body :prefList="prefList" />
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import Header from '~/components/index/organisms/Header.vue'
import Body from '../organisms/Body.vue'

export default Vue.extend({
  components: { Body },
  props: {
    prefList: {
      default: [],
      type: Array,
    },
  },
})
</script>
