<template>
    <div>12315465465</div>
</template>

<script>
import dataset from '../assets/data.json'
const data = dataset.objectives
export default {
  name: 'activities',
  data () {
    return {
      data: data
    }
  },
  props: {
    msg2: String
  }
}

</script>
<style scoped>

</style>
