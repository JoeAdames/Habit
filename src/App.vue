<template>
<div>
<Header @resetTracker='resetTracker' :goal='this.goal' :greet='this.greeted'/>
<Greeting v-if="this.greeted != true" @getUserInput='getUserInput'/>
<Tracker v-if="this.greeted == true" :tracking='this.track' :count='this.count' />
</div>
</template>
<script>
import Header from './components/Header'
import Greeting from './components/Greeting'
import Tracker from './components/Tracker'
export default {
  name: 'App',
  components: {
    Header,
    Greeting,
    Tracker
  },
  emit: ['resetTracker', 'getUserInput'],
  data () {
    return {
      track: null,
      count: null,
      check: null,
      goal: null
    }
  },
  methods: {
    resetTracker () {
      this.track = null
      this.count = null
      this.goal = null
      this.check = null
    },
    getUserInput (track, length, goal) {
      this.track = track
      this.count = parseInt(length)
      this.goal = parseInt(goal)
      this.check = true
    }
  }
}
</script>
<style>
</style>
