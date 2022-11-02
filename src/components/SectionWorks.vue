<script setup>
</script>

<template>
   <section id="section-works">
      <div class="container">
         <button type="button" class="arrow left"></button>

         <div class="wrap">
            <div class="view">
               <div class="pic">
                  <img src="../assets/LP_fb_01.jpg" alt="LP">
               </div>
               <a href="#" class="btn"><span>VIEW PROJECT</span><span class="btn-line"></span></a>
            </div>

            <div class="text fadeInUp wow" data-wow-duration="2s">
               <h5>HIGHLIGHTED SHOWCASE</h5>
               <h1 class="title">LP CLUB MOBILE APP</h1>
               <p class="fadeInUp wow" data-wow-duration="3s" data-wow-delay="0.2s" >Cras quis nulla commodo, aliquam lectus sed, blandit augue. Cras ullamcorper bibendum bibendum. Duis tincidunt urna non pretium porta. Nam condimentum vitae ligula vel ornare. Phasellus at semper turpis. Nunc eu tellus tortor. Etiam at condimentum nisl, vitae sagittis orci. Donec id dignissim nunc. Donec elit ante, eleifend a dolor et, venenatis facilisis dolor. In feugiat orci odio, sed lacinia sem elementum quis. Aliquam consectetur, eros et vulputate euismod, nunc leo tempor lacus, ac rhoncus neque eros nec lacus. Cras lobortis molestie faucibus.</p>
            </div>
         </div>

         <button type="button" class="arrow right"></button>
         
         <div class="page">
            <div class="number">01</div>
            <!-- <div class="divider"></div> -->
            <div class="number down">04</div>
         </div>
      </div>
   </section>
</template>

<style scoped>
#section-works {
   width: 100%;
   /* height: 100%; */
   background-image: url(../assets/BG_LP_fb.jpg);
   background-position: center;
   background-repeat: no-repeat;
   background-size: cover;
   border-radius: 0 0 50px 50px;
   display: flex;
   justify-content: center;
   align-items: center;
   /* position: relative; */
   padding-top: 10%;
   padding-bottom: 10%;
}
#section-works .container {
   display: flex;
   align-items: center;
   justify-content: space-between;
   /* margin-top: 600px;
   margin-bottom: 600px; */
   position: relative;
}

.arrow {
   width: 56px;
   height: 56px;
   background-color: #26C6D0;
   border-radius: 50%;
   border: 0;
   outline: 0;
   position: relative;
   box-shadow: 2px 2px 3px rgba(5, 96, 103, 0.8);
   cursor: pointer;
   transform: scale(1);
   transition: 0.3s;
}
.arrow::before {
   content: '';
   position: absolute;
   left: 55%;
   top: 50%;
   width: 30%;
   height: 30%;
   border-left: 3px solid #fff;
   border-bottom: 3px solid #fff;
   transform: translate(-50%, -50%) rotate(45deg);
}

.arrow.right::before {
   left: 50%;
   top: 50%;
   transform: translate(-50%, -50%) rotate(225deg);
}
.arrow:hover {
   /* filter: brightness(1.1); */
   background-color: #35d6e2;
   /* transform: scale(1.05); */
   box-shadow: 3px 3px 5px rgba(5, 96, 103, 0.8);
}
.arrow:active {
   transform: translateY(-0.5px) scale(.98);
}
.wrap {
   display: flex;
   width: 90%;
   /* height: 50%; */

   align-items: center;
   justify-content: space-around;
}
.view { 
   position: relative;
   width: 50%;
   padding: 3%;
   /* height: 100%; */

}

.view .pic {
   max-width: 540px;
   width: 100%;
   height: 100%;
   border-radius: 30px;
   overflow: hidden;
}
.view .btn {
   margin: 0;
   /* margin-left: 0;
   margin-right: 0;
   margin-top: 0; */
   padding: 35px 20px;
   position: absolute;
   bottom: 0;
   right: 0;
   /* bottom: -60px;
   right: -50px; */
   /* left: 70%; */
}
.text {
   width: 50%;
   padding: 3%;
}
.text h5 {
   font-style: normal;
   font-weight: 700;
   font-size: 16px;
   line-height: 19px;
   letter-spacing: 2px;
   color: #FFFFFF;
   padding-bottom: 3%;
}
.text .title {
   margin: 0;
   color: #ffff;
   display: inline-block;
}
.text .title:before {
   bottom: 5px;
   left: -5px;
   right: -5px;
   background-color:#26C6D0;
   height: 5px;
}
.text p {
   color: #ffff;
   text-align: left;
   line-height: 24px;
   padding-top: 8%;
}

.page {
   width: 54px;
   height: 54px;
   position: absolute;
   top: 0;
   right: 0;
   /* background-color: red; */
   /* margin-right: 60px; */
   margin-right: 6%;
   z-index: 10;
   background:
    linear-gradient(-45deg, transparent 48.5%, #26C6D0 48.5%, #26C6D0 50%, transparent 50%);

}

/* .page::after {
   content: '';
   position: absolute;
   left: 0;
   right: 0;
   width: 100%;
   border-bottom: 3px solid #26C6D0;
} */

.page .number {
   color: #fff;
   font-style: normal;
   font-weight: 600;
   font-size: 16px;
   line-height: 19px;
   letter-spacing: 2px;
   position: absolute;
   cursor: pointer;
}

.page .number.down {
   bottom: 0;
   right: 0;
}

@media(max-width: 992px) {
   .wrap {
      flex-direction: column;
      align-items: center;
      width: 70%;
   }
   .view {
      width: 100%;
      height: 300px;
      padding: 0
   }
   .view .pic {
      max-width: 100%;
      height: 80%;
   }
   .view .btn {
      bottom: 20%;
      right: -5%;
      transform: translate(0, 50%);
      padding: 15px 20px;
   }
   .text {
      width: 100%;
   }
}

@media(max-width: 576px) {
   #section-works {
      /* height: 100vh; */
      /* max-height: 1000px; */
      /* min-height: 100vh; */
      padding-top: 15%;
   }
   #section-works .container {
      padding-top: 20%;
      align-items: flex-start;
      width: 90%;
      padding-left: 0;
      padding-right: 0;
   }
   .wrap {
      width: 100%;
   }
   .view {
      padding: 5%;
      height: 100%;
      margin-bottom: 20%;
   }

   .view .btn {
      bottom: 5%;
      right: 0;
   }
   .text {
      width: 100%;
   }

   .text .title {
      font-size: 28px;
      letter-spacing: 1px;
   }

   .page {
     width: 44px;
     height: 44px;
   }

   .arrow {
      background-color: rgba(38,198,208,0.8);
      margin-top: 40%;
      width: 44px;
      height: 44px;
      position: absolute;
      z-index: 5;
   }
   .arrow.right {
      right: 0;
   }
}

@media(max-width: 340px) {
   .wrap {
      width: 100%;
   }

   .text .title {
      font-size: 24px;
      letter-spacing: 1px;
   }
}



</style>
