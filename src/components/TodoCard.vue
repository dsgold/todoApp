<template>

  <div class="flex flex-col w-72 h-72 rounded-lg shadow shadow-white drop-shadow-sm">
    <div class="flex-none border-gray-400 border-b">
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
      {{ this.cardName }}
      <br>
      {{ this.cardText }}
    </div>
    <div v-if="this.cardCheckList.length > 1" class="flex-none border-gray-400 border-t ">
      <div class="flex flex-row items-center p-1">
        <BaseIcon name="checked"/>
        <span class="pl-1">{{ this.cardCheckList[0] }}/{{ this.cardCheckList[1] }}</span>
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