<script setup>
</script>

<template>
  <section id="section-about-awards">
    <div class="taste line">
      <!-- <div class="pic">
        <img src="../assets/te.png" alt="taste">
      </div>
      <h6>TASTE US NOW!</h6> -->
      <div class="indicator-line"></div>
    </div>

    <div id="about">
      <div class="container fadeInUp wow" data-wow-duration="2s" data-wow-offset="2">
        <h2 class="title">ABOUT DIGISALAD</h2>
        <div class="video-container">
          <div class="video">
            <iframe frameborder="0" src="https://www.youtube.com/embed/IeIRJ9jZ5Ro" allowFullScreen="true"></iframe>
          </div>
        </div>
        <p>Cras quis nulla commodo, aliquam lectus sed, blandit augue. Cras ullamcorper bibendum bibendum. Duis tincidunt urna non pretium porta. Nam condimentum vitae ligula vel ornare. Phasellus at semper turpis. Nunc eu tellus tortor. Etiam at condimentum nisl, vitae sagittis orci. Donec id dignissim nunc. Donec elit ante, eleifend a dolor et, venenatis facilisis dolor. In feugiat orci odio, sed lacinia sem elementum quis. Aliquam consectetur, eros et vulputate euismod, nunc leo tempor lacus, ac rhoncus neque eros nec lacus. Cras lobortis molestie faucibus.</p>
        <a href="#" class="btn"><span>VIEW MORE</span><span class="btn-line"></span></a>
      </div>
    </div>

    <div id="awards" class="awards fadeInRight wow" data-wow-duration="1.5s">
      <div class="container">
        <div class="text">
          <h2 class="title">AWARDS</h2>
          <p>Cras quis nulla commodo, aliquam lectus sed, blandit augue. Cras ullamcorper bibendum bibendum. Duis tincidunt urna non pretium porta. Nam condimentum vitae ligula vel ornare. Phasellus at semper turpis. Nunc eu tellus tortor. Etiam at condimentum nisl, vitae sagittis orci. Donec id dignissim nunc.</p>
        </div>
        <div class="pic">
          <div class="row">
            <div class="col">
              <img src="../assets/image5.png">
            </div>
            <div class="col">
              <img src="../assets/image5.png">
            </div>
          </div>
          <div class="row">
            <div class="col">
              <img src="../assets/image5.png">
            </div>
            <div class="col">
              <img src="../assets/image5.png">
            </div>
          </div>
        </div>
      </div>
    </div>
    
  </section>

</template>

<style scoped>

#section-about-awards {
  width: 100%;
  /* height: 100vh; */
  background-color:#E5E5E5;
  position: relative;
}
.container {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: auto;
  padding-bottom: 216px;
  /* padding-bottom: 15%; */

}

p {
  max-width: 960px;
}
.video-container {
  max-width: 960px;
  margin: auto;
  padding: 0 80px;
  width: 100%;
  margin-bottom: 30px;
}
.video {
  position: relative;
  height: 0;
  padding-bottom: 56.25%;
  /* margin-bottom: 100px; */
}

.video iframe {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}

.btn {
  width: 223px;
  height: 86px;
}

/* 
 * awards
 */
.awards {
  background-color: #ffff;
  border-radius: 50px 0 50px 50px;
  width: 93%;
  /* width: 1280px; */
  /* height: 432px; */
  position: absolute;
  bottom: -216px;
  /* bottom: -15%; */
  right: 0;
  z-index: 1;
  display: flex;
  align-items: center;
  /* margin-left: 80px; */
  height: 33%;
}

.awards .container {
  flex-direction: row;
  justify-content: space-between;
  /* width: 1280px; */
  height: 100%;
  padding-top: 216px;
  /* padding-top: 15%; */
}

.awards .text {
  width: 35%;

}
.awards .title {
  /* display: inline-block; */
  margin: 0;
}
.awards p {
  text-align: left;
  font-size: 16px;
  font-weight: 400;
  line-height: 28px;
  letter-spacing: 1px;
  color: #262626;
  margin-top: 50px;
}



.awards .pic {
  width: 60%;
  display: flex;
  flex-direction: column;
}

.awards .row {
  width: 100%;
  margin: 3%;
  display: flex;
  /* justify-content: space-around; */
}


@media (max-width: 992px) {
  .container {
    /* padding-bottom: 60%; */
    padding-bottom: 350px;
  }
  .awards {
    bottom: -350px;
    /* bottom: -60%; */
    /* bottom: -50%; */
    /* height: 60%; */
    /* padding-bottom: 31%; */
    height: 700px;
    /* height: 30%; */
  }
  .awards .container {
    flex-direction: column;
    /* justify-content: flex-start; */
    justify-content: center;
    align-items: center;
    margin-right: 7%;
    height: 100%;
    padding-top: 350px;
    /* padding-left: 0;
    padding-right: 0; */
    /* padding-top: 60%; */
    /* padding-top: 20%; */
  }

  .awards .text {
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;

  }

  .awards p {
    padding: 5%;
    text-align:justify;
    text-justify:inter-ideograph;
    word-break: break-all;
    /* margin-top: 30px; */
  }

  .awards .pic {
    width: 100%;
  }

  .awards .row {
    justify-content: space-around;
    margin-left: 0;
  }

  .video-container {
    padding: 0;
  }
}

/* 
 * taste icon
 */
.taste {
  position: absolute;
  top: 0;
  left: 50%;
  transform: translateX(-50%);
  display: flex;
  flex-direction: column;
  align-items: center;
  z-index: 10;

}
.taste .indicator-line {
  width: 2px;
  height: 80px;
  background-color: #808080;
}

</style>
