<template>
 <div class="wrapper">
   <div class="card">
    <Logo />
    <Welcome />
    <LandingText />
    <email-form />
 </div>
 <div>
   <hero-cover-img />
 </div>
 </div>
</template>

<script>
import Logo from './components/Logo.vue'
import Welcome from './components/Welcome.vue'
import LandingText from './components/LandingText.vue'
import HeroCoverImg from './components/HeroCoverImg.vue'
import EmailForm from './components/EmailForm.vue'
export default {
  name: 'App',

  components: {
  Logo,
  Welcome,
  LandingText,
    HeroCoverImg,
    EmailForm,
  }

}
</script>

<style>
*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

.wrapper {
  display: flex;
  height: 500px;
  overflow: hidden;
  justify-content: center;
  align-items: center;
  padding: 20px 20px 10px 0;
}

.card{
 height: 500px;
 background-color: bisque;
 border: 1px solid #BEBEBE;
 justify-content: center;
 padding: 25px;
}
</style>
