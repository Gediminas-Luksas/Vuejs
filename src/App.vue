<template>
  <div id="app">
     <AppHeader :date="headerData">
         My day!
     </AppHeader>
     <div class="todo-list">
      <ul class="todo-list__list">
      <button 
        class="todo-list__input-button" 
        type="button"
        >
        Delete
        </button>
        <button 
        class="todo-list__input-button" 
        type="button"
        >
        Edit
        </button>
      {{ newTodo }}
      </ul>
      <TodoInput v-model="newTodo"/>
     </div>
  </div>
</template>

<script>
import AppHeader from '@/components/AppHeader'
import TodoInput from '@/components/TodoInput'
export default {
  name: 'App',
  components: {
    AppHeader,
    TodoInput
  },
  data: () => ({
    newTodo: null,
    headerData: new Date('2018,10,5')
  })
}
</script>

<style lang='scss'>

</style>
