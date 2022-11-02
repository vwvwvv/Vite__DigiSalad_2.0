<script setup>
import{ reactive } from 'vue'
const cards = reactive([
  {
    img: new URL("../assets/CardIngradients/ingradient_01.png", import.meta.url).href,
    item: 'UX Design'
  },
    {
    img: new URL("../assets/CardIngradients/ingradient_02.png", import.meta.url).href,
    item: 'UX Design'
  },
  {
    img: new URL("../assets/CardIngradients/ingradient_03.png", import.meta.url).href,
    item: 'website development'
  },
  {
    img: new URL("../assets/CardIngradients/ingradient_04.png", import.meta.url).href,
    item: 'mobile app development'
  },
  {
    img: new URL("../assets/CardIngradients/ingradient_05.png", import.meta.url).href,
    item: 'ecommerce'
  },
  {
    img: new URL("../assets/CardIngradients/ingradient_06.png", import.meta.url).href,
    item: 'customer loyalty'
  },
  {
    img: new URL("../assets/CardIngradients/ingradient_07.png", import.meta.url).href,
    item: 'digital transformation'
  },
  {
    img: new URL("../assets/CardIngradients/ingradient_08.png", import.meta.url).href,
    item: 'digital marketing'
  },
  {
    img: new URL("../assets/CardIngradients/ingradient_09.png", import.meta.url).href,
    item: 'BRANDING'
  }

])
</script>

<template>
  <div id="card-ingradient" v-for="card in cards" :key='card'>
    <div class="wrap">
      <div class="pic bounceIn wow" data-wow-duration="1s" ata-wow-delay="1s">
        <img :src="card.img" alt="">
      </div>
      <div class="text">
        <h4>{{ card.item }}</h4>
        <p>Cras quis nulla commodo, aliquam lectus sed, blandit augue. Cras ullamcorper bibendum bibendum. Duis tincidunt urna non pretium porta. Nam condimentum vitae ligula vel ornare.</p>
      </div>
    </div>
    <a href="#">VIEW MORE</a>
  </div>
</template>

<style scoped>
#card-ingradient {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  width: 25%;
  margin-bottom: 65px;
  margin-left: 20px;
  margin-right: 20px;
}

.wrap{
  display: flex;
  flex-direction: column;
  align-items: center;
}

.pic {
  border-radius: 50%;
  width: 108px;
  height: 108px;
  padding: 20px;
  background-color:#fff;
  overflow: hidden;
  transform: scale(1);
  transition: 0.5s;
}
.pic:hover {
  transform: scale(1.15);

}

img {
  width: 100%;
  height: 100%;
  object-fit: contain;
  display: block;
}
.text {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

h4 {
  font-style: normal;
  font-weight: 700;
  font-size: 20px;
  line-height: 24px;
  letter-spacing: 2px;
  text-transform: uppercase;
  color: #fff;
  margin: 10%;
  text-align: center;
  display: flex;
  justify-content: center;
  align-items: center;
  max-width: 250px;
  height: 30px;
}

p {
  color: #fff;
  width: auto;
  /* padding: 20px 0; */
}

a {
  display: block;
  text-decoration: none;
  padding: 18px 35px;
  border-radius: 50px;
  background-color: transparent;
  border: 3px solid #fff;
  color: #fff;
  font-style: normal;
  font-weight: 700;
  font-size: 14px;
  line-height: 17px;
  letter-spacing: 2px;
  margin: 6%;
  transition: 0.5s;
}

a:hover {
  box-shadow: inset 0 0 6px 2px rgba(255, 255, 255, 0.8);
}

@media (max-width: 992px) {
  a {
    padding: 18px 23px;
  }
}

@media (max-width: 768px) {
  #card-ingradient {
    width: 40%;
  }
}

@media (max-width: 576px) {
  #card-ingradient {
    width: 100%;
    margin-bottom: 30%;
  }
}
</style>
