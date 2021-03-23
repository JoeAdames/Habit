<template>
<div class="container">
<Card :title='this.tracking' :count='this.count'/>
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
    count: Number
  }
}
</script>
<style>
.container {
  padding: 10px;
  width: 100%;
}
</style>
