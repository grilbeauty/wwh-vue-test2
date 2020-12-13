<template>
  <li>
    <span class="red" v-if="!del">{{ value }}</span>
    <span v-else style="background-color: aquamarine">{{ value }}</span>
    <button v-show="!del" @click="handleClick">删除</button>
  </li>
</template>
<script>
export default {
  props: {
    value: String,
    del: {
      Type: Boolean,
      default: false
    }
  },
  data () {
    return {}
  },
  methods: {
    handleClick () {
      console.log('aaa')
      this.$emit('delete', this.value)
    }
  }
}
</script>
<style scoped>
.red{
    color: red;
}
</style>
