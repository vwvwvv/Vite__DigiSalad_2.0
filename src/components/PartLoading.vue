<script setup>
import { onMounted } from 'vue'

onMounted(() => {
  const addEventOnElements = function (elem, type, callback) {
    for (let i = 0; i < elem.length; i++) {
      elem[i].addEventListener(type, callback);
    }
  }
  
  const loadingElement = document.querySelector('data-loading-container')

  window.addEventListener('load', () => {
    loadingElement.classList.add('loaded')
    document.body.classList.add('loaded')
  })
})

</script>

<template>
  <div id="loading-container" data-loading-container>
    <div class="loading-circle"></div>
  </div>
</template>

<style scoped>

body {
  height: 300vh;
  overflow: hidden;
}

body.loading {
  overflow: visible;
}
body.active {
  overflow: hidden;
}

#loading-container {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100vh;
  background-color: rgb(247, 247, 247);

  display: grid;
  place-items: center;
  transition: 0.5s;
  z-index: 9999;

  display: none;
}

#loading-container.loaded {
  opacity: 0;
  visibility: hidden;
}

.loading-circle {

  width: 50px;
  height: 50px;
  border: 5px solid #EE6C8A;
  border-block-start-color: #26C6D0;
  border-radius: 50%;
  animation: loading 0.5s linear infinite;
}
@keyframes loading {
  0% { transform: rotate(0);}
  100% { transform: rotate(360deg);}
}

#loading-cotainer.loaded,
.loading-circle {
  animation-iteration-count: 1;
}
</style>
