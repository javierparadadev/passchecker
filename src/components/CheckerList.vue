<script setup>
import PassCheckerItem from './PassCheckerItem.vue'
import DocumentationIcon from './icons/IconDocumentation.vue'
import ToolingIcon from './icons/IconTooling.vue'
</script>

<template>
  <PassCheckerItem>
    <template #icon>
      <DocumentationIcon />
    </template>
    <template #heading>Ibelynx Algorithm</template>

    Ibelynx’s
    <a href="https://vuejs.org/" target="_blank" rel="noopener">password strength algorithm</a>.

  </PassCheckerItem>

  <PassCheckerItem>
    <template #icon>
      <ToolingIcon />
    </template>
    <template #heading>zxcvbn</template>

    Algorithm, developed by <a href="https://vitejs.dev/guide/features.html" target="_blank" rel="noopener">Dropbox</a>, 
    assesses password strength by estimating the number of attempts 
    needed for an attacker to guess it. It evaluates against common passwords, keyboard patterns, demographic data, 
    and accounts for both offline and online attack scenarios.

  </PassCheckerItem>

</template>
