<script setup>
import ImageItem from "./ImageItem.vue"
</script>

<template>
  <div id="Galerie">
    <a>
      <h1 id="ListBoxHeader">3D</h1>
    </a>
    <div class="ListBox" id="ListContainer">
        <ul>
          <li v-for="image in imageList">
            <ImageItem 
            :icon=image.icon
            :textDescription="image.text"
            :header="image.heading"
            >
          </ImageItem>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
import ImageList from "../assets/imageList.json";
export default {
  name: "Art",
  components: {},
  data() {
    return {
      imageList: ImageList,
    };
  },
  mounted() {

  }
  }
  </script>
  
  
<style>
.ListBox{
  border: 1px solid var(--color-background);
  border-radius: 25px;
  height: 40vh;
  overflow: auto;
  text-overflow: clip;
  display: flex;
  align-content: center;
}
.ListBox a {
  display: block;
}
#Galerie ul{
  padding: 0;
  list-style-type: none;
  display: flex;
  flex-direction: row;
  flex-wrap: nowrap;
  justify-content: center;
}
#Galerie ul li{
  margin: 5px;
  border-radius: 5px;
  display: flex;
  flex-grow: 1;
  justify-content: center;
  align-self: center;
}
</style>

