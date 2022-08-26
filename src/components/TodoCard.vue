<template>
  <div class="flex flex-col border border-black w-72 h-72">
    <div class="flex-none border-black border-b">
      <div class="flex p-1">
        <span class="left-0">Card tags</span>
        <div class="flex ml-auto">
          <BaseIcon name="minus"/>
          <BaseIcon name="bigger"/>
          <BaseIcon name="xMark"/>
        </div>
      </div>
    </div>
    <div class="grow p-5 al">
      {{this.cardName}}
      <br>
      {{this.cardText}}
    </div>
    <div class="flex-none border-black border-t">
      <div v-if="this.cardCheckList.length > 1" class="flex flex-row items-center p-1">
        <BaseIcon name="checked"/>
        <span class="pl-1">{{this.cardCheckList[0]}}/{{this.cardCheckList[1]}}</span>
      </div>
    </div>
  </div>
</template>

<script>
import BaseIcon from "./BaseIcon.vue";
export default {
  name: "TodoCard",
  components: {
    BaseIcon,
  },
  props: {
    cardId: {
      type: Number,
      required: true
    },
    cardName: {
      type: String,
      required: true
    },
    cardText: {
      type: String,
      required: false
    },
    cardCheckList: {
      type: Array,
      required: false
    }
  }
}
</script>

<style scoped>

</style>