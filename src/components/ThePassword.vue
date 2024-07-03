<template>
  <input
    class="input is-primary"
    type="text"
    placeholder="Write your password here..."
    :value="password"
    @input="updateValue"
  />
</template>
  
<script>
export default {
  name: 'ThePassword',
  props: ['password'],
  methods: {
    updateValue(event) {
      this.$emit('password-change', event.target.value);
    }
  }
}
</script>

  
<style scoped>
  input {
    width: 100%;
    margin-bottom: 2rem;
    margin-top: 2rem;
  }
</style>
  