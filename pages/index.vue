<template>
  <div class="index-pages">
    <indexTemplates :prefList="prefList" />
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import indexTemplates from '../components/index/templates/index.vue'
import $axios from '@nuxtjs/axios'
export default Vue.extend({
  components: { indexTemplates },
  async asyncData({ $axios }) {
    const url = 'https://opendata.resas-portal.go.jp/api/v1/prefectures'
    const response = await $axios.$get(url, {
      headers: { 'X-API-KEY': process.env.API_KEY },
    })
    return { prefList: response.result }
  },
})
</script>
