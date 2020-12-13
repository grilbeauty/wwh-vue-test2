<template>
  <div id="app">
    {{ message }}
    <div :id="message"></div>
    <todo-list></todo-list>
  </div>
</template>

<script>
// eslint-disable-next-line no-unused-vars
import TodoList from './components/TodoList.vue'
export default {
  name: 'App',
  components: {
    TodoList

  },
  data () {
    return {
      message: 'hello'
    }
  }
}
</script>
