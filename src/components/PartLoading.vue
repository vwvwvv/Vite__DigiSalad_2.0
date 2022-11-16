<script setup>
import { onMounted } from 'vue'

onMounted(() => {

  // =============================================
  // add event on multiple elements
  // =============================================
  const addEventOnElements = function (elem, type, callback) {
    for (let i = 0; i < elem.length; i++) {
      elem[i].addEventListener(type, callback);
    }
  }


  // =============================================
  // Loading
  // =============================================
  // const loadingElement = document.querySelector('[data-loading-container]')
  const loadingElement = document.querySelector('.loading-container')

  window.addEventListener('load', () => {
    loadingElement.classList.add('js-loaded')
    document.body.classList.add('js-loaded')
  })
})

</script>

<template>
  <div id="loading">
    <div class="loading-container" data-loading-container>
      <div class="loading-circle"></div>
    </div>
</div>
</template>

<style scoped>

.loading-container {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100vh;
  background-color: #26C6D0;

  display: grid;
  place-items: center;
  transition: 0.5s;
  z-index: 999999999999999;
  /* display: none; */
}

.loading-circle {
  width: 50px;
  height: 50px;
  border: 5px solid #fff;
  border-block-start-color: #EE6C8A;
  border-radius: 50%;

  animation-name: loading;
  animation-duration: 0.3s;
  animation-timing-function: linear;
  animation-iteration-count: infinite;
}

@keyframes loading {
  0% { transform: rotate(0);}
  100% { transform: rotate(1turn);}
}

/*
 *---------------------------------------------------
 *當網頁loading讀取資料結束後會隱藏loading圖案+次數變轉一次
 *---------------------------------------------------
 */
.loading-container.js-loaded {
  opacity: 0;
  visibility: hidden;
}
.loading-container.js-loaded .loading-circle {
  /* 動畫劇本重複次數 */
  animation-iteration-count: 1;
}
</style>
