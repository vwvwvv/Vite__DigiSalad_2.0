<script setup>
import CardIngradients from './CardIngradients.vue'
</script>

<template>
  <section id="section-service-founder">
    <div class="service">
      <div class="container">
        <div class="info">
          <h2 class="title" id="service">
            OUR INGREDIENTS
          </h2>
          <p>
            Cras quis nulla commodo, aliquam lectus sed, blandit augue. Cras ullamcorper bibendum bibendum. Duis tincidunt urna non pretium porta. Nam condimentum vitae ligula vel ornare. Phasellus at semper turpis. Nunc eu tellus tortor. Etiam at condimentum nisl, vitae sagittis orci. Donec id dignissim nunc. Donec elit ante, eleifend a dolor et, venenatis facilisis dolor. In feugiat orci odio, sed lacinia sem elementum quis. Aliquam consectetur, eros et vulputate euismod, nunc leo tempor lacus, ac rhoncus neque eros nec lacus. Cras lobortis molestie faucibus.
          </p>
          <a href="#" class="btn">
            <span>OUR SERVICES</span><span class="btn-line"></span>
          </a>
        </div>

        <div class="card-wrap">
          <CardIngradients></CardIngradients>
        </div>
        <a href="#" class="more-btn">
            VIEW MORE <br class="md-none" />DIGISALAD’S INGRADIENTS
        </a>
      </div>
    </div>
    
    <div class="founder">
      <div class="container fadeInLeft wow" data-wow-duration="1s">
        <div class="character">
          <div class="avatar">
            <img src="../assets/TST1914.jpg" alt="avatar">
          </div>
          <h4 class="name">Tony Ng</h4>
          <div class="position">Founder & Creative Director</div>
        </div>
         
        <div class="text">
          <div class="icon">
            <img src="../assets/left-quote.png" alt="quote">
          </div>
          <p>
            A great digital work isn’t about designing beautiful pages purely. It is about context - how do we deliver the <span>right experience to the right person at the right time.</span>The most important thing is that your work can engage customers at anytime, anywhere and let users experience an entire amazing digital journey.
          </p>
        </div>
      </div>
    </div>

  </section>
</template>

<style scoped>

#section-service-founder {
  width: 100%;
  background-color:#26C6D0;
  border-radius: 50px 50px 0 0 ;
  position: relative;
  padding-bottom: 433px;
  text-align: center;
}


#section-service-founder::before {
  content: '';
  position: absolute;
  inset: 0;
  background-color:#E5E5E5;
  z-index: -1;
}

.info {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: auto;
  padding-top: 216px;
}

.title {
  color:#FFFFFF;
}

.title::before {
  background-image: url(../assets/wave585880.png);
}

.btn {
  width: 294px;
  height: 92px;
  background-color: #585880;
}

.info p {
  /* max-width: 960px; */
  color:#FFFFFF;
}



/* --------------------------------*\
 card 
\* --------------------------------*/
.card-wrap {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}

.more-btn {
  display: inline-block;
  text-decoration: none;
  text-align: center;
  font-style: normal;
  font-weight: 700;
  font-size: 18px;
  line-height: 22px;
  letter-spacing: 2px;
  text-transform: uppercase;
  color: #FFFFFF;
  position: relative;
  z-index: 1;
}
.more-btn::after {
  content: '';
  position: absolute;
  left: -5px;
  right: -5px;
  bottom: 1px;
  height: 10px;
  background-color:#FFBC58;
  z-index: -1;
  transition: 0.5s;
}

.more-btn:hover::after {
  background-color:#d6993e;
}

.md-none {
  display: none;
}



/* --------------------------------*\
 founder 
\* --------------------------------*/
.founder {
  background-color: #ffff;
  border-radius: 0 50px 50px 50px;
  /* max-width: 1280px; */
  width: 90%;
  height: 23%;
  /* height: 598px; */
  position: absolute;
  bottom: -299px;
  left: 0;
  z-index: 1;

  display: flex;
  align-items: center;

  background-image: url(../assets/shutterstock_675737842.jpg);
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}

.founder .container {
  display: flex;
  align-items: center;
  justify-content: space-around;
  width: 1280px;
  height: 100%;
}

.founder .character {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-right: 50px;
}

.founder .avatar {
  width: 204px;
  height: 204px;
  border-radius: 50%;
  overflow: hidden;
  margin-bottom: 15%;
}

.founder .name {
  font-style: normal;
  font-weight: 700;
  font-size: 20px;
  line-height: 24px;
  text-align: center;
  letter-spacing: 2px;
  text-transform: uppercase;
  color: #FFFFFF;
}

.founder .position {
  font-style: italic;
  font-weight: 400;
  font-size: 16px;
  line-height: 16px;
  text-align: center;
  letter-spacing: 2px;
  color: #FFFFFF;
  padding-top: 3%;
}
.founder .text {
  display: flex;
  flex-direction: column;
  align-items: center;
}
.founder .icon {
  width: 90px;
  height: 90px;
  overflow: hidden;
  margin: 20px;
}

.founder p {
  font-style: normal;
  font-weight: 400;
  font-size: 22px;
  line-height: 48px;
  letter-spacing: 2px;
  color: #fff;
  text-align: left;
  max-width: 800px;
}

.founder p span {
  color: #FFBC58;
}


@media (max-width: 992px) {
  .info {
    padding-top: 350px;
  }
  #section-03 {
    padding-bottom: calc(100px + 500px);
  }
  .founder {
    bottom: -500px;
    height: 1000px;
    width: 94%;
  }
  .founder .container {
    flex-direction: column-reverse;
    padding-left: 10%;
    padding-top: 5%;
    padding-bottom: 5%;
  }
  .founder .character {
    margin-right: 0;
  }
  .founder p {
    text-align:justify;
    text-justify:inter-ideograph;
    word-break: break-all;
    padding-left: 3%;
    padding-right: 3%;
  }
}

@media (max-width: 576px) {
  .md-none {
    display: block;
  }

  .founder .icon  {
    width: 70px;
    height: 70px;
    /* margin-top: 5px; */
  }
  .founder p {
    font-size: 20px;
    line-height: 30px;

  }
}
@media (max-width: 377px) {
.founder .icon  {
    width: 55px;
    height: 55px;
    /* margin-top: 5px; */
    margin: 10px;
  }
  .founder p {
    font-size: 20px;
    line-height: 38px;
  }
}

@media (max-width: 340px) {
  .founder .icon  {
    width: 45px;
    height: 45px;
  }
  .founder p {
    font-size: 20px;
    letter-spacing: 2px;
    line-height: 34px;
  }
}

</style>
