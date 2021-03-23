<template>
<div>
<nav class="navbar navbar-expand-lg navbar-dark bg-primary">
  <div class="navbar-brand" href="#">Habit Tracker</div>
  <div v-if='this.check != null' class="flex">
  <div class="nav-link">Goal per day: {{ this.goal }}</div>
  <div class="nav-link">Current Amount: {{ this.counter }}</div>
  </div>
  <button class="btn btn-primary my-2 my-sm-0" type="submit" @click="$emit('resetTracker')">Reset</button>
</nav>
</div>
</template>
<script>
export default {
  name: 'Header',
  props: {
    goal: Number,
    check: Boolean
  },
  data () {
    return {
      currentGoal: null,
      counter: 0
    }
  }
}
</script>
<style scoped>
.flex {
  display: flex;
  flex-direction: column;
  flex-wrap: wrap;
}
</style>
