<template>
  <div class="page">
    <todo-input-text
      v-model="newTodoText"
      placeholder="just input what you will do" 
      @enter="addTodo"
    />
    <ul v-if="todos.length">
      <todo-list-item 
        v-for="todo in todos"
        :key="todo.id"
        :todo="todo"
        @remove="removeTodo"
        />
    </ul>
    <p v-else>
      Please add a new todo in the input above.
    </p>

  </div>
</template>

<script>
import TodoInputText from './TodoInputText.vue'
import TodoListItem from './TodoListItem.vue'

let nextTodoId = 1

export default {
  name: 'TodoList',
  data () {
    return {
      newTodoText: '',
      todos: [{id:nextTodoId++, text:'222'}]
    }
  },
  components: {
    'todo-input-text': TodoInputText,
    'todo-list-item': TodoListItem
  },
  methods: {
    //enter键添加todo item
    addTodo () {
      const trimmedText = this.newTodoText.trim()
      if (trimmedText) {
        this.todos.push({
          id: nextTodoId++,
          text: trimmedText
        })
        this.newTodoText = ''
      }
    },
    //X键移除todo item
    removeTodo (idToRemove) {
      this.todos = this.todos.filter(todo => {
        return todo.id !== idToRemove
      })
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
