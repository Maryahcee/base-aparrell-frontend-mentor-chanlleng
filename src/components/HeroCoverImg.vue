<template>
  <div>
  <img :src="HeroCoverImg">
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

</style>