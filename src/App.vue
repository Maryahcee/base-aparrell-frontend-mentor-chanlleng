<template>
 <div class="card">
    <Logo />
    <Welcome />
    <LandingText />
    <email-btn />
 </div>
</template>

<script>
import Logo from './components/Logo.vue'
import Welcome from './components/Welcome.vue'
import LandingText from './components/LandingText.vue'
import EmailBtn from './components/EmailBtn.vue'
export default {
  name: 'App',

  components: {
  Logo,
  Welcome,
  LandingText,
    EmailBtn,
  }

}
</script>

<style>
*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

.card{
  width: 500px;
  height: 500px;
 background-color: bisque;
 border: 1px solid #BEBEBE;
 justify-content: center;
}
</style>
