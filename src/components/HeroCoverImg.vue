<template>
  <div class="image-container">
  <img :src="HeroCoverImg" class="hero-img">
  </div>
</template>

<script>
import HeroCoverImg from  '../assets/images/hero-desktop.jpg'

export default {
name: 'Hero',
props: '',

data: function() {
    return{
        HeroCoverImg,
    }
}
}
</script>

<style>
.image-container {
  max-width: 100%;
  max-height: 100%;
}

.hero-img {
  height: 555px;
}

</style>