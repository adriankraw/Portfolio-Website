<script setup>
import ImageItem from "./ImageItem.vue"
</script>

<template>
  <div id="Galerie">
    <fieldset class="ListBox" :class="{active: boxListactive}">
      <legend>
        <h1 id="ListBoxHeader">Art</h1>
      </legend>
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
    </fieldset>
    <button @click="boxListactive = !boxListactive" id="EndIcon"><h1>v</h1></button>
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
      boxListactive: false,
    };
  },
}
function Toggle(){
  console.log(this.boxListactive);
}
</script>

<style>
.ListBox{
  border: 1px solid var(--color-background);
  border-radius: 25px;
  height: 40vh;
  overflow: hidden;
}
.active{
  height: 90vh;
  overflow: auto;
}
#EndIcon{
  top: -35px;
  width: 100%;
  display: flex;
  justify-content: center;
  background-color: var(--color-background);
  border-radius: 50px;
  cursor: pointer;
  z-index: 4;
}
#EndIcon:hover{
  background-color: var(--color-background-soft);
}
#Galerie ul{
  padding: 0;
  list-style-type: none;
  display: flex;
  flex-wrap: wrap;
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

