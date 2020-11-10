<template>
  <div class="home">
    <HelloWorld msg="Welcome to Your Vue.js App" />
    <Add @addItem="addItem"/>
    <List :listData="listData"/>
  </div>
</template>

<script>
import HelloWorld from '@/components/HelloWorld.vue'
import Add from '@/components/Add.vue'
import List from '@/components/List.vue'
export default {
  name: 'Home',
  data () {
    return {
      listData: [
        {
          id: 1,
          text: '学习VUE',
          state: 0
        }
      ]
    }
  },
  methods: {
    addItem (item) {
      console.log(item)
      this.listData.push({ id: Date.now(), text: item, state: 0 })
    }
  },
  components: {
    HelloWorld,
    Add,
    List
  }
}
</script>
