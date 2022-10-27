<script setup>
</script>

<template>
  <div id="section-01">
    <div class="container">

      <div class="digital-agency">
        <div class="line"></div>
        <h6>DIGITAL AGENCY</h6>
      </div>

      <div class="hero-content">
        <h1 class="logo">
          <img src="../assets/logoW.png" alt="logo">
        </h1>
        <h2 class="slogan">
          WE CREATE<br/>
          AMAZING<br/>
          <span class="last-line">DIGITAL <br class="md-block"/>
          EXPERIENCES</span>
        </h2>
      </div>

      <div class="taste">
        <div class="pic">
          <a href="#anchor">
            <img src="../assets/te.png" alt="taste">
          </a>
        </div>
        <h6>TASTE US NOW!</h6>
        <div class="indicator-line"></div>
      </div>

    </div>

  </div>
</template>

<style scoped>
* { transition: 0.3s; }

#section-01 {
  width: 100%;
  height: 100%;
  /* height: 940px; */
  background-image: url(@/assets/BG.jpg);
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  border-radius: 0 0 50px 50px;
}
.container {
  /* width: 100%; */
  width: 1440px;
  /* position: relative; */
  /* display: flex; */
}
.digital-agency  {
  display: flex;
  align-items: center;
  justify-content: space-between;
  position: absolute;
  width: 300px;
  transform-origin: right top;
  transform: rotate(-90deg) translateX(50%);
  /* top: 249px; */
  /* left: -228.5px; */
  top: 50vh;
  right: 95%;
}
.digital-agency .line {
  width: 113px;
  height: 2px;
  background-color: #fff ;
  /* margin-right: 24px; */
}

.digital-agency h6 {
  font-size: 16px;
  font-weight: 700;
  line-height: 20px;
  letter-spacing: 2px;
  color: #fff;
}

.hero-content {
  position: absolute;

  /* top: 181px;
  left: 220px; */
  /* margin-top: 15%; */
  /* width: 100%; */

  /* width: 10%; */
  left: 15%;
  top: 20vh;
  text-shadow: 0 0 20px rgba(0,0,0,0.5);
  z-index: 1;
}

.hero-content .logo {
  width: 200px;
  margin-bottom: 5%;
}

.hero-content .slogan {
  font-weight: 700;
  font-size: 38px;
  color: #fff;
  line-height: 70px;
  letter-spacing: 10px;
}
.hero-content .md-block {
  display: none;
}



/**
 * taste [scroll down]
 */
.last-line:before {
  content: '';
  position: absolute;
  bottom: 17px;
  left: -5px;
  right: 5px;
  background-color:#26C6D0;
  display: inline-block;
  height: 15px;
  z-index: -1;
}

.last-line::after {
  content: '';
  position: absolute;
  bottom: 20px;
  right: -15px;
  background-color:#EE6C8A;
  width: 10px;
  height: 10px;
  border-radius: 50%;
  z-index: -1;
}









/**
 * taste [scroll down]
 */
.taste {
  position: absolute;
  bottom: 0;
  left: 50%;
  transform: translateX(-50%);
  display: flex;
  flex-direction: column;
  align-items: center;
  z-index: 1;
  cursor: pointer;
  /* margin-top: 20%; */
}
.taste a {
  text-decoration: none;
}
.taste .pic {
  width: 65px;
  height: 65px;
  border-radius: 50%;
  overflow: hidden;
  box-shadow: 0 0 8px rgba(0, 0, 0, 0.7);
  transform: scale(1);
  transition: 0.5s;

}
.taste:hover .pic {
  transform: scale(1.1);
}
.taste h6 {
  font-style: normal;
  font-weight: 700;
  font-size: 14px;
  line-height: 17px;
  letter-spacing: 2px;
  text-transform: uppercase;
  text-align: center;
  color: #FFFFFF;
  padding-top: 10px;
  padding-bottom: 30px;
}

.taste .indicator-line {
  width: 1px;
  height: 50px;
  background-color: #fff;
}

@media (max-width: 769px) {
  .hero-content .md-block {
    display: block;
  }

}

@media (max-width: 576px) {
  .hamburger {
    margin-left: 20px;
  }
  .digital-agency {
    /* display: none; */
    transform: rotate(0deg);
    transform-origin: left top;
    bottom: 5vh;
    left: 5%;
    width: 80%;
  }
  .hero-content {
    left: 6%;
    top: 25vh;
  }
  .hero-content .logo {
    width: 200px;
    margin-bottom: 10%;
  }
  .hero-content .slogan {
    font-weight: 700;
    font-size: 38px;
    color: #fff;
    line-height: 60px;
    letter-spacing: 8px;
  }

  .last-line:before {
    bottom: 10px;
    left: -5px;
    right: 5px;
    height: 12px;
    background:#26C6D0;
    /* background:linear-gradient(180deg, transparent 20%, #26C6D0 100%); */
  }

  .last-line::after {
    bottom: 20px;
    right: -15px;
    width: 10px;
    height: 10px;
  }

  .taste {
    bottom: -3%;
  }

}

@media (max-width: 377px) {

  .hero-content {
    top: 22vh;
  }

   .hero-content .slogan {
    font-size: 36px;
    line-height: 50px;
    letter-spacing: 8px;
  }

}

@media (max-width: 340px) {

  .hero-content {
    top: 23vh;
  }
  .hero-content .slogan {
    font-size: 25px;
    line-height: 35px;
  }

    .last-line:before {
    bottom: 3px;
    left: -5px;
    right: 5px;
  }

  .last-line::after {
    bottom: 15px;
    right: -25px;
    width: 15px;
    height: 15px;
  }

  .hero-content .logo {
    width: 130px;
  }
  .digital-agency {
    bottom: 18vh;
    left: 5%;
    width: 90%;
  }

}


</style>
