<template>
  <div id="template">
    <div class="details">
      <h3>{{ props.header }}</h3>
      <br>
      <div>{{ props.textDescription }}</div>
    </div>
    <div class="item">
      <i id="image">
        <img v-bind:src=props.icon alt="" />
      </i>
    </div>
  </div>
</template>

<script setup>

const props = defineProps({
  header: {type: String, default:"Header"},
  icon: {type: String, default:""},
  textDescription: {type: String, default: "empty text"}
})


</script>

<style scoped>
#template:hover .details{
  height: 45%;
}
#image{
  display: flex;
  object-fit: cover;
  justify-content: center;
  overflow: hidden;
  max-width: 34vw;
  height: 400px;
  transition: height 2s, width 2s;
  transition-timing-function: ease;
}
.details{
  height: 2em;
  transition: height 1s;
  transition-timing-function: ease;
  position: absolute;
  display: flex;
  flex-direction: column;
  justify-content: start;
  overflow: hidden;
  bottom: 0;
  width: 100%;
  z-index: 2;
  background-color: rgba(225, 225, 225, 0.76);
  color: black;
}
.details > *{
  margin: 0px 10px 0px 10px;
}
</style>
