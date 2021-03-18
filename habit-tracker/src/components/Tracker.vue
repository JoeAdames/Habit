<template>
<div>
<Card :title='this.tracking' />
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
    tracking: String
  }
}
</script>
<style>
</style>
