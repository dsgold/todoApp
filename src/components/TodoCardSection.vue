<template>
  <div class="flex flex-col">
    <div v-for="todo in todoCards" class="m-5">
      <TodoCard
          :card-id="todo.cardID"
          :card-name="todo.cardName"
          :card-text="todo.cardText"
          :card-check-list="todo.cardCheckList"/>
    </div>
  </div>
</template>

<script>
import TodoCard from "./TodoCard.vue";

export default {
  name: "TodoCardSection",
  components: {TodoCard},
  data() {
    return {
      todoCards: [
        {
          cardID: 1,
          cardName: 'First task',
          cardText: 'Create base card component',
          cardCheckList: [2, 5]
        },
        {
          cardID: 2,
          cardName: 'Second task',
          cardText: 'Create section for cards',
          cardCheckList: [3, 6]
        },
        {
          cardID: 3,
          cardName: 'Third task',
          cardText: 'Create full todos holder',
          cardCheckList: [0]
        }
      ],
    }
  },
}
</script>

<style scoped>

</style>