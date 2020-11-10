<template>
  <div>
    <input type="text" v-model="inputData" />
    <button @click="addItem">add</button>
  </div>
</template>

<script>
export default {
  name: 'Add',
  data () {
    return {
      inputData: ''
    }
  },
  methods: {
    addItem () {
      if (this.inputData) {
        this.$emit('addItem', this.inputData)
        this.inputData = ''
      }
    }
  }
}
</script>

<style>
</style>
