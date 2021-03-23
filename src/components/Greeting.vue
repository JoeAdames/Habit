<template>
<div class="container">
<div class="form-group flex">
<label>What would you like to track?</label>
<input v-model="userInput" />
<label>For how many days?</label>
<input v-model="userCount" />
<label>What is your per day goal?</label>
<input v-model="userGoal" />
<button class="btn btn-secondary my-2 my-sm-0"  @click="$emit('getUserInput', userInput, userCount, userGoal)">Submit</button>
</div>
</div>
</template>
<script>
export default {
  name: 'Greeting',
  data () {
    return {
      userInput: null,
      userCount: null,
      userGoal: null
    }
  }
}
</script>
<style scoped>
input {
  width: 200px;
}
button {
  margin-top: 10px;
  max-width: 200px;
}
.container {
  max-height: 500px;
  max-width: 500px;
}
.flex {
  display: flex;
  flex-direction: column;
  justify-content: center;
}
</style>
