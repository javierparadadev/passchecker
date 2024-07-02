<template>
    <input
      class="input is-primary"
      type="text"
      placeholder="Write your password here..."
    />
</template>
  
  <script>
  export default {
    name: 'ThePassword',
    data() {
      return {
        inputValue: ''
      };
    }
  }
  </script>
  
<style scoped>
  input {
    width: 100%;
  }
</style>
  