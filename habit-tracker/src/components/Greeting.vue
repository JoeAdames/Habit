<template>
<div>
<div class="form-group">
<label for="inputSmall">What would you like to track?</label>
<input v-model="userInput" />
<button @click="$emit('getUserInput', this.userInput)">Submit</button>
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
