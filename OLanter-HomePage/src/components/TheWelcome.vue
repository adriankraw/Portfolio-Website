<script setup>
import Topper from './main/Topper.vue';
</script>

<template>
  <div class="rootheader">
    <header>
      <Topper />
      <br>
      <div id="body">
        My Name is Adrian Krawczyk. I am developer / programmer, specialized in Unity-Development. 
        While creating various tools and thinking about new features, I find myself looking at art.
        Trying to a create a shader to emphasize the look of specific materials & textures has become a passion of mine.
      </div>
    </header>
    <div id="Skillset"> 
      <h1>Skillset</h1>
      <ul>
        <li>3DModelling</li>
        <li>Programming
          <ul>
            <li>C#</li>
          </ul>
        </li>
        <li>Drawing</li>
      </ul>
      <br>
      <h1>Software</h1>
      <ul>
        <li>Unity3D</li>
        <li>Blender</li>
      </ul>
    </div>
  </div>
</template>

<style>
header {
  line-height: 1.5;
}
.rootheader {
  display: flex;
  flex-direction: row;
  flex-grow: 1;
  justify-content: center;
  margin: 0 10vh 0 10vh;
}
.rootheader header{
  max-width: 40vw;
  margin-right: 2em;
}
</style>
