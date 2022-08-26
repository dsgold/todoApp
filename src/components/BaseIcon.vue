<template>
  <svg
      xmlns="http://www.w3.org/2000/svg"
      fill="none"
      viewBox="0 0 24 24"
      :stroke="this.color || 'currentColor'"
      class="w-6 h-6 items-center"
      v-html="path"
  >
  </svg>
</template>

<script>
import icons from "../icons.js";

export default {
  name: "BaseIcon",
  props: ['name', 'color'],
  data() {
    return {
      path: icons[this.name]
    }
  }
}
</script>

<style scoped>

</style>

