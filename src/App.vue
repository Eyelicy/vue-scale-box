<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup
import ScaleBox from './components/scaleBox'
</script>

<template>
  <scale-box :width="1920" :height="1080" class="scale-box">
    <img alt="Vue logo" src="./assets/logo.png" />
  </scale-box>
</template>

<style>
html,
body,
#app {
  padding: 0;
  margin: 0;
  width: 100%;
  height: 100%;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background: red;
}
</style>
