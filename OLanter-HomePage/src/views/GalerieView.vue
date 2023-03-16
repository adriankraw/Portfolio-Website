<script setup>
import Item from "../components/WelcomeItem.vue"
</script>

<template>
  <div id="Galerie">
    <ul>
      <li v-for="image in imageList">
        <Item>
          <template #icon>
            <img id="singleImage" :src= image.icon alt="asd" /></template>
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
        { icon: "../src/assets/images/The_Forest.jpg", heading: "cat King"},
        { icon: "../src/assets/images/Dragon—tree.png", heading: "cat King"},
        { icon: "../src/assets/images/Elf-portrait.jpg", heading: "cat King"},
        { icon: "../src/assets/images/Forest-Girl-27-12.jpg", heading: "cat King"},
      ]
    };
  }
}
</script>

<style>
#Galerie ul{
  padding: 0;
  list-style-type: none;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
}
#Galerie ul li{
  margin: 5px;
  border-radius: 5px;
  display: flex;
  justify-content: center;
  align-self: center;
  overflow: hidden;
}
#Galerie ul li:hover .details{
  height: 45%;
}
#singleImage {
  width: 24vw;
  height: 400px;
  object-fit: cover;
  overflow: none;
}
</style>

