<template>
<div class='flex'>
<div v-for="index in count" :key='index' class="card text-white bg-primary mb-3" style="max-width: 20rem; min-width: 20rem;">
  <div class="card-header">Day {{ index }}</div>
  <div class="card-body">
    <h4 class="card-title" @click="log(index++)" >{{ title }}</h4>
    <input type="text" placeholder="How many?" v-model='newNumber'>
    <button @click="dayFinished()" class="finish btn btn-primary my-2 my-sm-0">Finish</button>
  </div>
</div>
</div>
</template>
<script>
export default {
  name: 'Card',
  props: {
    title: String,
    count: Number
  },
  data () {
    return {
      counter: null,
      newNumber: null
    }
  },
  methods: {
    log (it) {
      console.log(it)
    },
    dayFinished () {

    }
  }
}
</script>
<style scoped>
.flex {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
}
.finish {
  margin-left: 10px;
}
</style>
