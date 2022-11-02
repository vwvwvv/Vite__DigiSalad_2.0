<script setup>
import { onMounted } from 'vue'

onMounted( () => {
  const hamburgerIcon = document.querySelector('.hamburger-icon')
  const navigation = document.querySelector('.navigation')
  const about = document.querySelector('.about')
  hamburgerIcon.addEventListener('click', function () {
    hamburgerIcon.classList.toggle('active')
    navigation.classList.toggle('active')
  })
  about.addEventListener('click', function () {
    navigation.classList.toggle('active')
    hamburgerIcon.classList.toggle('active')
  })
})

</script>

<template>
  <header>
    <div class="container full">
      <h1 class="logo">
        <a href="#"><img src="@/assets/logoO.png" alt="logo"></a>
      </h1>
      <div class="menu">
        <button type="button" class="btn-start">START YOUR PROJECT</button>
        <div class="hamburger-icon">
          <span class="hamburger-icon__line"></span>
        </div>
      </div>

      <ul class="navigation">
        <li><a href="#about" class="about">about</a></li>
        <li><a href="#works" class="works">works</a></li>
        <li><a href="#" class="careers">careers</a></li>
        <li><a href="#" class="insignts">insignts</a></li>
        <li><a href="#" class="services">services</a></li>
        <li><a href="#" class="contact">contact</a></li>
      </ul>
    </div>
  </header>
</template>

<style scoped>

.full {
  min-width: 100vw;
  height: 100px;
  padding-left: 5%;
  padding-right: 5%;
  background-color: rgba(255, 255, 255, 0.5); 
  /* background-color: transparent; */
}
.container {
  display: flex;
  align-items: center;
  justify-content: space-between;
  position: fixed;
  z-index: 9999;
}
h1.logo {
  height: 54px;
  /* opacity: 0; */
}

.menu {
  display: flex;
  align-items:center;
  justify-content: space-between;
}

/**
 * ----------------------------------------
 * btn-start
 * ----------------------------------------
 */
.btn-start {
  width: 200px;
  height: 40px;
  border-radius: 24px;
  border: 0;
  /* background-image:linear-gradient(to right, #4EE5EA 3.94%, #26D0A8 94.73%); */
  background-image:linear-gradient(120deg, #4EE5EA 10%, #00ffc3 60%,#0015ff7d 90%, #26D0A8 100%);
  font-style: normal;
  font-weight: 700;
  font-size: 14px;
  line-height: 17px;
  letter-spacing: 1.2px;
  color: #FFFFFF;
  cursor: pointer;
  transition: 1.5s;
  background-size: 400% auto;
  text-shadow: 0 0 4px rgba(2, 139, 111, 0.2);
}

.btn-start:hover {
  /* background:linear-gradient(45deg, #26D0A8 3.94%, #4EE5EA 94.73%); */
  background-position: right center;
  box-shadow: 0 0 5px rgba(8, 58, 46, 0.5);
}
.btn-start:active {
  transform: scale(0.7);
  box-shadow: inset 0 0 3px 1px rgba(0, 0, 0, 0.2);
}

/**
 * ----------------------------------------
 * 漢堡 ICON
 * ----------------------------------------
 */

 .hamburger-icon {
  cursor: pointer;
  position: relative;
  width: 30px;
  height: 22px;
  z-index: 9999;
  margin-left: 50px;
  top: -1px;
}

.hamburger-icon__line,
.hamburger-icon::before,
.hamburger-icon::after {
  display: block;
  width: 100%;
  height: 4px;
  background-color: #FFFF;
  border-radius: 100px;
  position: absolute;
  transition: 0.2s;
}

/* part-navbar.stick .hamburger-line,
#part-navbar.stick .hamburger::before,
#part-navbar.stick .hamburger::after {
  background-color:#414042;
} */

.hamburger-icon__line {
  top: 50%;
  transform: translateY(-50%);
}

.hamburger-icon::before {
  content: '';
  top: 0;
}

.hamburger-icon::after {
  content: '';
  bottom: 0;
  right: 0;
  width: 80%;
}




.hamburger-icon.active .hamburger-icon__line { display: none;}
.hamburger-icon.active::before,
.hamburger-icon.active:after {
  top: 50%;
  transform: translateY(-50%);
  background-color:rgba(255,255,255,1);
}
.hamburger-icon.active::before {
  transform: rotate(45deg);
}
.hamburger-icon.active::after {
  width: 100%;
  transform: rotate(-45deg);
}

.navigation { display: none }
.navigation.active {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(180deg, rgba(88, 88, 128, 0.5) 3.61%, rgba(38, 198, 208, 0.5) 95.7%);
  /* background: linear-gradient(180deg, rgba(88, 88, 128, 0.5) 3.61%, rgba(38, 198, 208, 0.5) 95.7%), url(@/assets/BG.jpg);
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover; */
  display: flex;
}

header ul li { list-style: none; }

header ul li a {
  display: inline-block;
  color: black;
  text-decoration: none;
  user-select: none;
  padding: 8px 18px;
}

</style>
