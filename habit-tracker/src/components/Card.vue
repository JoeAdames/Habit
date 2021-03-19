<template>
<div>
<div v-for="index in this.length" :key='index' class="card text-white bg-primary mb-3" style="max-width: 20rem;">
  <div class="card-header">{{ title }}</div>
  <div class="card-body">
    <h4 class="card-title" @click="log(index++)" >Day {{ index }}</h4>
    <p class="card-text">Blah</p>
  </div>
</div>
</div>
</template>
<script>
export default {
  name: 'Card',
  props: {
    title: String,
    length: Number
  },
  data () {
    return {
      counter: 0
    }
  },
  methods: {
    log (it) {
      console.log(it)
    }
  }
}
</script>
<style>
</style>
