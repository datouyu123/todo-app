<template>
  <div class="page">
    <todo-input-text
      v-model="newTodoText"
      placeholder="just input what you will do" 
    />
  </div>
</template>

<script>
import TodoInputText from './TodoInputText.vue'


export default {
  name: 'TodoList',
  data () {
    return {
      newTodoText: '',
    }
  },
  components: {
    'todo-input-text': TodoInputText
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
