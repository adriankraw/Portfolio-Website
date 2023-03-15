<script setup>
import Item from "../components/WelcomeItem.vue"
</script>

<template>
  <div id="Galerie">
    <ul>
      <li v-for="image in imageList">
        <Item>
          <template #icon>
            <img id="singleImage" :src= image.icon alt="asd" /> </template>
          <template #heading>{{ image.heading }}</template>
        </Item>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "Art",
  components: {},

  data() {
    return {
      imageList: [
        { icon: "../src/assets/images/Tree_120420.jpg", heading: "Tree" }, 
        { icon: "../src/assets/images/cat_-King_2.jpg", heading: "cat King"},
        { icon: "../src/assets/images/cat_-King_2.jpg", heading: "cat King"},
        { icon: "../src/assets/images/cat_-King_2.jpg", heading: "cat King"},
        { icon: "../src/assets/images/cat_-King_2.jpg", heading: "cat King"},
        { icon: "../src/assets/images/cat_-King_2.jpg", heading: "cat King"},
        { icon: "../src/assets/images/cat_-King_2.jpg", heading: "cat King"},
      ]
    };
  }
}
</script>

<style scoped>
#Galerie{
  width: 80vw;
}
template {
  max-height: 90vh;
}
#Galerie ul{
  padding: 0;
  list-style-type: none;
  display: grid;
  grid-auto-flow: column;
  align-items: start;
  justify-content: start;
}
#Galerie ul li{
  margin-bottom: 1em;
  background-color: grey;
  margin: 5px;
  border-radius: 5px;
}
#singleImage {
  max-width: 400px;
  max-height: 400px;
}
</style>

