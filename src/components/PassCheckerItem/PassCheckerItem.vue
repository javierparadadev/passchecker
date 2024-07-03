<script setup>
  import { ref, watchEffect, onMounted } from 'vue';

  const props = defineProps({
    functionKey: String
  });

  const functionsDict = {
    librelynx: pwd => 100,
    zxcvbn: pwd => 100,
  };

  const currentFunction = ref(() => {});

  watchEffect(() => {
    currentFunction.value = functionsDict[props.functionKey] || (() => console.log('Función no definida'));
  });

  onMounted(() => {
    currentFunction.value();
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

      <progress class="progress is-success is-small" value="60" max="100"/>
    </div>
    
  </div>
</template>

<style src="./styles.css" scoped></style>
