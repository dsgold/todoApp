<template>
  <div class="flex">
    <TodoCardSection/>
    <TodoCardSection/>
    <TodoCardSection/>
    <TodoCardSection/>
  </div>
</template>

<script>

import TodoCardSection from "./components/TodoCardSection.vue";

export default {
  name: 'App',
  components: {
    TodoCardSection
  }
}
</script>

<style>

</style>
