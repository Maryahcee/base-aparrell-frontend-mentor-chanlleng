<template>
  <div class="logo">
  <img :src="logo">
  </div>
</template>

<script>
import logo from  '../assets/images/logo.svg'

export default {
name: 'Logo',
props: '',

data: function() {
    return{
        logo,
    }
}
}
</script>

<style>

</style>