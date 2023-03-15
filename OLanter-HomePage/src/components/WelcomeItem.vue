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
#image {
  height: 40vh;
  width: 40vw;
}
</style>
