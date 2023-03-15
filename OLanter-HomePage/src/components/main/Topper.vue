<script setup>
import HelloWorld from "../../components/HelloWorld.vue";
import LogoIcon from "../../components/icons/Logo.vue"
</script>

<template>
    <div id="topper">
      <LogoIcon />
      <HelloWorld msg="Adrian K." />
    </div>
</template>

<style scoped>
#topper {
  display: flex;
  flex-direction: row;
}
</style>