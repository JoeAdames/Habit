<template>
<div>
<Greeting v-if="this.greeted != true" @get-user-input='getUserInput'/>
<Tracker v-if="this.greeted == true" :tracking='this.track' :length='this.count' />
</div>
</template>
<script>
import Greeting from './components/Greeting'
import Tracker from './components/Tracker'
export default {
  name: 'App',
  components: {
    Greeting,
    Tracker
  },
  emit: ['getUserInput'],
  data () {
    return {
      track: String,
      count: Number,
      greeted: Boolean
    }
  },
  methods: {
    getUserInput (track, length) {
      this.track = track
      this.count = length
      console.log(this.track, this.count)
      this.greeted = true
    }
  }
}
</script>
<style>
</style>
