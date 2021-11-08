<template>
  <div class="scale-box">
    <slot></slot>
  </div>
</template>

<script setup>
import { ref, onMounted, defineProps } from 'vue'
const width = ref(null),
  height = ref(null),
  scale = ref(null)

const props = defineProps({
  width: {
    type: Number,
    required: false,
    default: '1920',
  },
  height: {
    type: Number,
    required: false,
    default: '1080',
  },
})

width.value = props.width + 'px'
height.value = props.height + 'px'

const init = () => {
  setScale()
  window.addEventListener('resize', setScale)
}

function setScale() {
  let ww = window.innerWidth / props.width
  let wh = window.innerHeight / props.height
  scale.value = ww < wh ? ww : wh
}

init()
</script>

<style scoped>
.scale-box {
  width: v-bind(width);
  height: v-bind(height);
  transform: scale(v-bind(scale)) translate(-50%, -50%);
  transform-origin: 0 0;
  position: absolute;
  left: 50%;
  top: 50%;
  transition: 0.3s;
}
</style>
