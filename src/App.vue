<template>
  <router-view/>
</template>
<script>
import dataset from './assets/data.json'
const data = dataset.jiasong
// console.log(data)
export default {
  name: 'App',
  data () {
    return {
      data: data
    }
  },
  props: {
    msg: String
  }
}
</script>
<style>
</style>
