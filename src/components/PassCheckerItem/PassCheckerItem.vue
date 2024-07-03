<script setup>
  import { ref, watchEffect, watch } from 'vue';
  import zxcvbn from 'zxcvbn';

  const props = defineProps({
    functionKey: String,
    password: String,
  });

  const functionsDict = {
    librelynx: pwd => pwd.length * 2,
    zxcvbn: pwd => zxcvbn(pwd).score * 25,
  };

  const currentFunction = ref(() => {});
  const functionResult = ref(0);

  watchEffect(() => {
    currentFunction.value = functionsDict[props.functionKey] || (() => console.log('Función no definida'));
  });

  watch(() => props.password, (newPassword) => {
    functionResult.value = currentFunction.value(newPassword);
  }, { immediate: true });

</script>

<template>
  <div class="item">
    <i>
      <slot name="icon"></slot>
    </i>
    <div class="details">
      <h3>
        <slot name="heading"></slot>
      </h3>

      <slot></slot>

      <progress class="progress is-success is-small" :value="functionResult" max="100"/>
    </div>
    
  </div>
</template>

<style src="./styles.css" scoped></style>
