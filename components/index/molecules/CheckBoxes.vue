<template>
  <div class="index-molecules-check-boxes">
    <div v-for="value in prefNameList" :key="value.toString()">
      <CheckBox :boxText="value" />
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import CheckBox from '../atoms/CheckBox.vue'

export default Vue.extend({
  components: { CheckBox },
  data() {
    return {
      prefNameList: [
        '北海道',
        '青森県',
        '岩手県',
        '秋田県',
        '山形県',
        '宮城県',
        '福島県',
      ],
    }
  },
})
</script>

<style scoped>
.index-molecules-check-boxes {
  display: flex;
  flex-wrap: wrap;
  padding: 0 10px;
}
</style>
