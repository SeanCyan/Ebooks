<script setup>
import 'vue3-carousel/carousel.css'
import { Carousel, Slide, Navigation } from 'vue3-carousel'


const imagesL = [
 {
  id: 1,
  url: `https://raw.githubusercontent.com/SeanCyan/Portfolio/refs/heads/master/img/Ebook/22P1.png`
 },
 {
  id: 2,
  url: `https://raw.githubusercontent.com/SeanCyan/Portfolio/refs/heads/master/img/Ebook/22P2.png`
 },
 {
  id: 3,
  url: `https://raw.githubusercontent.com/SeanCyan/Portfolio/refs/heads/master/img/Ebook/22P3.png`
 },
 {
  id: 4,
  url: `https://raw.githubusercontent.com/SeanCyan/Portfolio/refs/heads/master/img/Ebook/22P4.jpg`
 },
 {
  id: 5,
  url: `https://raw.githubusercontent.com/SeanCyan/Portfolio/refs/heads/master/img/Ebook/22P5.png`
 },
 {
  id: 6,
  url: `https://raw.githubusercontent.com/SeanCyan/Portfolio/refs/heads/master/img/Ebook/22P6.png`
 },
 {
  id: 7,
  url: `https://raw.githubusercontent.com/SeanCyan/Portfolio/refs/heads/master/img/Ebook/22P7.png`
 },
 {
  id: 8,
  url: `https://raw.githubusercontent.com/SeanCyan/Portfolio/refs/heads/master/img/Ebook/22P8.png`
 },
]

const imagesP = [
 {
  id: 9,
  url: `https://raw.githubusercontent.com/SeanCyan/Portfolio/refs/heads/master/img/Ebook/23P1.png`
 },
 {
  id: 10,
  url: `https://raw.githubusercontent.com/SeanCyan/Portfolio/refs/heads/master/img/Ebook/23P2.png`
 },
 {
  id: 11,
  url: `https://raw.githubusercontent.com/SeanCyan/Portfolio/refs/heads/master/img/Ebook/23P3.png`
 },
 {
  id: 12,
  url: `https://raw.githubusercontent.com/SeanCyan/Portfolio/refs/heads/master/img/Ebook/23P4.png`
 },
 {
  id: 13,
  url: `https://raw.githubusercontent.com/SeanCyan/Portfolio/refs/heads/master/img/Ebook/23P5.png`
 },
 {
  id: 14,
  url: `https://raw.githubusercontent.com/SeanCyan/Portfolio/refs/heads/master/img/Ebook/23P6.png`
 },
 {
  id: 15,
  url: `https://raw.githubusercontent.com/SeanCyan/Portfolio/refs/heads/master/img/Ebook/23P7.png`
 },
 {
  id: 16,
  url: `https://raw.githubusercontent.com/SeanCyan/Portfolio/refs/heads/master/img/Ebook/23P8.png`
 },
]


const images = [
{
  id: 1,
  url: `https://raw.githubusercontent.com/SeanCyan/Portfolio/refs/heads/master/img/Ebook/22P1.png`
 },
 {
  id: 2,
  url: `https://raw.githubusercontent.com/SeanCyan/Portfolio/refs/heads/master/img/Ebook/22P2.png`
 },
 {
  id: 3,
  url: `https://raw.githubusercontent.com/SeanCyan/Portfolio/refs/heads/master/img/Ebook/22P3.png`
 },
 {
  id: 4,
  url: `https://raw.githubusercontent.com/SeanCyan/Portfolio/refs/heads/master/img/Ebook/22P4.jpg`
 },
 {
  id: 5,
  url: `https://raw.githubusercontent.com/SeanCyan/Portfolio/refs/heads/master/img/Ebook/22P5.png`
 },
 {
  id: 6,
  url: `https://raw.githubusercontent.com/SeanCyan/Portfolio/refs/heads/master/img/Ebook/22P6.png`
 },
 {
  id: 7,
  url: `https://raw.githubusercontent.com/SeanCyan/Portfolio/refs/heads/master/img/Ebook/22P7.png`
 },
 {
  id: 8,
  url: `https://raw.githubusercontent.com/SeanCyan/Portfolio/refs/heads/master/img/Ebook/22P8.png`
 },
{
  id: 9,
  url: `https://raw.githubusercontent.com/SeanCyan/Portfolio/refs/heads/master/img/Ebook/23P1.png`
 },
 {
  id: 10,
  url: `https://raw.githubusercontent.com/SeanCyan/Portfolio/refs/heads/master/img/Ebook/23P2.png`
 },
 {
  id: 11,
  url: `https://raw.githubusercontent.com/SeanCyan/Portfolio/refs/heads/master/img/Ebook/23P3.png`
 },
 {
  id: 12,
  url: `https://raw.githubusercontent.com/SeanCyan/Portfolio/refs/heads/master/img/Ebook/23P4.png`
 },
 {
  id: 13,
  url: `https://raw.githubusercontent.com/SeanCyan/Portfolio/refs/heads/master/img/Ebook/23P5.png`
 },
 {
  id: 14,
  url: `https://raw.githubusercontent.com/SeanCyan/Portfolio/refs/heads/master/img/Ebook/23P6.png`
 },
 {
  id: 15,
  url: `https://raw.githubusercontent.com/SeanCyan/Portfolio/refs/heads/master/img/Ebook/23P7.png`
 },
 {
  id: 16,
  url: `https://raw.githubusercontent.com/SeanCyan/Portfolio/refs/heads/master/img/Ebook/23P8.png`
 },
]


console.log(images);


const carousel1config = {
 itemsToShow: 5,
 gap: 10,
 wrapAround: true,
}

const carousel2config = {
 itemsToShow: 5,
 gap: 10,
 wrapAround: true,
}

const carouselConfig = {
  dir: 'ttb',
  wrapAround: true,
  itemsToShow: 5,
  snapAlign: 'center',
  height: 'auto',
  gap: 1,
}
</script>


<template>

 <Carousel v-bind="carousel1config" id="landscape">
  <Slide v-for="image in imagesL" :key="image.id">
   <img :src="image.url" alt="image" />
  </Slide>


  <template #addons>
   <Navigation />
  </template>
 </Carousel>

 <Carousel v-bind="carousel2config" id="portrait">
  <Slide v-for="image in imagesP" :key="image.id">
   <img :src="image.url" alt="image" />
  </Slide>


  <template #addons>
   <Navigation />
  </template>
 </Carousel>

 <Carousel v-bind="carouselConfig" id="vertical">
    <Slide v-for="img in images" :key="img.id">
      <img :src="img.url" />
    </Slide>

    <template #addons>
      <Navigation />
      <Pagination />
    </template>
  </Carousel>

</template>


<style>
:root {
 background-color: #f9eeff;
}
body { margin:0px; }

.carousel {
 --vc-nav-background: rgba(255, 255, 255, 0.7);
 --vc-nav-border-radius: 100%;
 width:98vw;
 margin:20px auto;
}
.carousel__viewport { border-radius:10px;}
#landscape {
  height: 30vh;
}


img {
 border-radius: 20px;
 width: 100%;
 height:auto;
 object-fit: contain;
 -webkit-box-shadow: 0px 0px 32px -8px rgba(0,0,0,0.2);
-moz-box-shadow: 0px 0px 32px -8px rgba(0,0,0,0.2);
box-shadow: 0px 0px 32px -8px rgba(0,0,0,0.2);
margin-top: 25px;margin-bottom:10px;
}
.carousel__next,
.carousel__prev {
 background: rgba(0, 0, 0, 0.3);
 border-radius: 50%;
 width: 40px;
 height: 40px;
 color: white;
 margin: 10px;
}
img[src*="Ebook22"] { 
  width:600px; 
}
#vertical {
    display: none;
  }
  @media all and (max-width: 1025px) {
  #landscape, #portrait {
    display: none;
  }
  #app {
    margin: 0 0px;
  }
  .carousel {
 --vc-nav-background: rgba(255, 255, 255, 0.7);
 --vc-nav-border-radius: 100%;
 width:100%;
 margin:20px auto;
}
  #vertical {
    display: block;
    position: fixed;
    bottom: 0;
    height: 90vh;
    width: 90vw;
    left:0;right:0;
  }
    #vertical li {
    height: auto !important;
    padding: 5px 0;
  }
  #vertical img {
    width: 100%;
    height: auto;
    background-size:contain;
  }

}
</style>

