<script setup>
  import { ref, watchEffect, onMounted } from 'vue';

  const props = defineProps({
    functionKey: String,
    password: String,
  });

  const functionsDict = {
    librelynx: pwd => 70-pwd.length,
    zxcvbn: pwd => 98-pwd.length,
  };

  const currentFunction = ref(() => {});
  const functionResult = ref(0);

  watchEffect(() => {
    currentFunction.value = functionsDict[props.functionKey] || (() => console.log('Función no definida'));
  });

  onMounted(() => {
    functionResult.value = currentFunction.value(props.password);
  });

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
