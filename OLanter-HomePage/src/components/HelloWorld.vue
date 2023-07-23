<script setup>
defineProps({
  msg: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <div class="greetings">
    <h1 class="green">{{ msg }}</h1>
    <h3> Developer / Programmer </h3>
    <br>
    <a class="Logo" href="https://www.artstation.com/olantern">Artstation</a>
  </div>
</template>

<style scoped>
.Logo{
  font-size: large;
  text-decoration: underline;
}

h1 {
  font-weight: 500;
  font-size: 2.6rem;
  margin-top: 10px;
  text-align: left;
}

h3 {
  font-size: 1.2rem;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>
