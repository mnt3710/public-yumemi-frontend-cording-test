<template>
  <div class="index-molecules-check-boxes">
    <div v-for="value of prefList" :key="value.prefCode">
      <CheckBox :boxText="value.prefName" @onChecked="addCheckedList" />
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import CheckBox from '../atoms/CheckBox.vue'

type DataType = {
  checkedValueList: Array<string>
  vForKey: number
}

export default Vue.extend({
  components: { CheckBox },
  data(): DataType {
    return {
      checkedValueList: [],
      vForKey: 0,
    }
  },
  props: {
    prefList: {
      default: '',
      type: Array,
    },
  },
  methods: {
    addCheckedList(value: string) {
      const checkedPositionList = this.checkedValueList.findIndex(
        (x) => x == value
      )
      checkedPositionList != -1
        ? this.checkedValueList.splice(checkedPositionList, 1)
        : this.checkedValueList.push(value)
    },
  },
})
</script>

<style scoped>
.index-molecules-check-boxes {
  display: flex;
  flex-wrap: wrap;
  margin: 5px 20px;
  outline-style: solid;
}
</style>
