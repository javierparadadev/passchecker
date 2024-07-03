<script setup>
import PassCheckerItem from './PassCheckerItem/PassCheckerItem.vue'
import CatIcon from './icons/IconCat.vue'
import ToolingIcon from './icons/IconTooling.vue'
</script>

<template>
  
  <PassCheckerItem>
    <template #icon>
      <CatIcon />
    </template>
    <template #heading>LibreLynx</template>

    <a href="https://www.librelynx.com/" target="_blank" rel="noopener">LibreLynx</a>’s password strength algorithm.

  </PassCheckerItem>

  <PassCheckerItem>
    <template #icon>
      <ToolingIcon />
    </template>
    <template #heading>zxcvbn</template>

    Algorithm, developed by <a href="https://www.dropbox.com/" target="_blank" rel="noopener">Dropbox</a>, 
    assesses password strength by estimating the number of attempts 
    needed for an attacker to guess it. It evaluates against common passwords, keyboard patterns, demographic data, 
    and accounts for both offline and online attack scenarios.

  </PassCheckerItem>

</template>
