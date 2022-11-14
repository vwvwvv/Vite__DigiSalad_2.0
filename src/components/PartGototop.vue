<script setup>
import { onMounted } from 'vue'
onMounted(() => {
  const go_to_top = document.getElementById('go-to-top')

  // ==================
  // 視窗往下滾
  // ==================
  window.addEventListener('scroll', function(){
    if(window.pageYOffset > 500){
      go_to_top.classList.add('js-show')
    }else {
       go_to_top.classList.remove('js-show')
    }
  })

  // ==================
  // 點擊回最上方
  // ==================
  go_to_top.addEventListener('click', function(){
    window.scrollTo({
      top: 0,
      left: 0
    })
  })
})
</script>

<template>
  <div id="go-to-top">
    <div class="arrow"></div>
  </div>
</template>

<style scoped>

#go-to-top {
  background-color: rgba(238, 108, 138, 0.9);
  width: 45px;
  height: 45px;
  border-radius: 50%;
  position: fixed;
  bottom: 5%;
  right: 5%;
  cursor: pointer;
  opacity: 0;
  transition: all 0.3s ease-in-out;
  z-index: 30;
}
#go-to-top.js-show {
  opacity: 1;
}
.arrow {
  position: absolute;
  inset: 15px;
  border-top: 3px solid #fff;
  border-left: 3px solid #fff;
  transform: translateY(3px) rotate(45deg);
}
</style>
