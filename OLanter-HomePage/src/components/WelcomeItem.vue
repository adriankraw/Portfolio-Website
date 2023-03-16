<template>
  <div class="details">
    <h3>
      <slot name="heading"></slot>
    </h3>
  </div>
  <div class="item">
    <i id="image">
      <slot name="icon">
        <img src="../assets/images/Tree_120420.jpg" alt="" />
      </slot>
    </i>
  </div>
</template>

<style scoped>
#image{
  display: flex;
}
.details{
  height: 2em;
  transition: height 1s;
  transition-timing-function: ease;

  position: absolute;
  display: block;
  bottom: 0;
  width: 100%;
  z-index: 2;
  background-color: rgba(225, 225, 225, 0.76);
  color: black;

  display: flex;
  justify-content: center;
}
</style>
