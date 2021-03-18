<template>
<div class="card text-white bg-primary mb-3" style="max-width: 20rem;">
  <div class="card-header">{{ title }}</div>
  <div class="card-body">
    <h4 class="card-title">Day</h4>
    <p class="card-text">Blah</p>
  </div>
</div>
</template>
<script>
export default {
  name: 'Card',
  props: {
    title: String
  }
}
</script>
<style>
</style>
