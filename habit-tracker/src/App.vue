<template>
<div>
<Greeting v-if="this.greeted != true" @get-user-input='getUserInput'/>
<Tracker v-if="this.greeted == true" :tracking='this.track' />
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
      greeted: Boolean
    }
  },
  methods: {
    getUserInput (track) {
      this.track = track
      console.log(this.track)
      this.greeted = true
    }
  }
}
</script>
<style>
</style>
