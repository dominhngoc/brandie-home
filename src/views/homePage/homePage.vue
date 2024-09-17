<script setup>
// import dependency
import homePageHeader from './components/homePageHeader.vue';
import homePageMain from './components/homePageMain.vue';
</script>
<template>
  <body class="text-black">
    <homePageHeader class="container"></homePageHeader>
  <!-- Main Section -->
  <homePageMain class="container"></homePageMain>
  </body>

</template>

<style>
html {
  font-family: "Readex Pro", sans-serif;
}
.container {
  @apply w-[70%] mx-auto;
}
</style>