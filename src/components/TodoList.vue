<template>
            <ul>
                <todo-item :key="item.value" @delete="handleDelete" v-for="item in list" :value="item.value" :del="item.del"></todo-item>
            </ul>
</template>
<script>
// eslint-disable-next-line no-unused-vars
import TodoItem from './TodoItem.vue'
export default {
  components: {
    TodoItem
  },
  data: function () {
    return {
      list: [
        {
          value: '课程一',
          del: false
        },
        {
          value: '课程二',
          del: true
        }
      ]
    }
  },
  methods: {
    handleDelete (val) {
      console.log('handleDelete', val)
    }
  }
}
</script>
