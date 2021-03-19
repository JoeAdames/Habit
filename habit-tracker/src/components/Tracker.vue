<template>
<div>
<Card :title='this.tracking' :length='this.length'/>
</div>
</template>
<script>
import Card from './Card.vue'
export default {
  name: 'Tracker',
  components: {
    Card
  },
  props: {
    tracking: String,
    length: Number
  }
}
</script>
<style>
</style>
