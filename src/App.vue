<template>
  <div class="main">
    <div class="header">
      <div class="header-text">
        <span>
          Kunstgallerie
        </span>
      </div>
    </div>
    <div class="line"></div>
    <div class="gallery">
      <Gallery/>
    </div>
  </div>

</template>

<script>
import Gallery from './components/Gallery.vue'

export default {
  name: 'App',
  components: {
    Gallery
  },  
}
</script>

<style>
#app {
  font-family: 'Open Sans', sans-serif;
}

.main{
display: flex;
flex-direction: column;
align-items: flex-start;
padding: 0px;
gap: 10px;
width: 1440px;
height: 644px;
}

.header{
display: flex;
flex-direction: row;
align-items: flex-start;
padding: 60px 182px;
gap: 10px;
box-sizing: border-box;
width: 1440px;
height: 194px;
}

.header-text{
display: flex;
flex-direction: column;
align-items: flex-start;
padding: 0px;
gap: 10px;
width: 418px;
height: 74px;
}

.header-text span{
width: 418px;
height: 74px;
font-family: 'Open Sans', sans-serif;
font-style: normal;
font-weight: 600;
font-size: 64px;
line-height: 115%;
color: #000000;
}

.line{
width: 1440px;
height: 1px;
background: #D9D9D9;
}

.gallery{
display: flex;
flex-direction: column;
align-items: flex-start;
padding: 10px 182px;
gap: 60px;
width: 1440px;
height: 429px;
}

</style>
