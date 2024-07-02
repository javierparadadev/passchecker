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
    <template #heading>Tooling</template>

    This project is served and bundled with
    <a href="https://vitejs.dev/guide/features.html" target="_blank" rel="noopener">Vite</a>. The
    recommended IDE setup is
    <a href="https://code.visualstudio.com/" target="_blank" rel="noopener">VSCode</a> +
    <a href="https://github.com/johnsoncodehk/volar" target="_blank" rel="noopener">Volar</a>. If
    you need to test your components and web pages, check out
    <a href="https://www.cypress.io/" target="_blank" rel="noopener">Cypress</a> and
    <a href="https://on.cypress.io/component" target="_blank" rel="noopener"
      >Cypress Component Testing</a
    >.

    <br />

    More instructions are available in <code>README.md</code>.
  </PassCheckerItem>

</template>
