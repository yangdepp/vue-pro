<template>
  <div>
    <ul v-for="item in listData" :key="item.id">
      <li>
        {{item.text}}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: {
    listData: {
      type: Array,
      required: true
    }
  }
}
</script>

<style>
</style>
