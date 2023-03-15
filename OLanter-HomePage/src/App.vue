<script setup>
import Topper from "./components/main/Topper.vue"
import Footer from "./components/main/Footer.vue"
</script>

<template>
  <router-view>
  </router-view>
<br>
  <Footer />
</template>

<style scoped>

#body {
  height: 100%;
  text-align: left;
  overflow: auto;
}
nav a:first-of-type {
  border: 0;
}

</style>
