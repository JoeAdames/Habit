<template>
<div>
<div class="form-group">
<label>What would you like to track?</label>
<input v-model="userInput" />
<label>For how many days?</label>
<input v-model="userCount" />
<button @click="$emit('getUserInput', this.userInput, this.userCount)">Submit</button>
</div>
</div>
</template>
<script>
export default {
  name: 'Greeting'
}
</script>
<style>
</style>
