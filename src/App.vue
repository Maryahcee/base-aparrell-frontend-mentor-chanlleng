<template>
    <mobile-view id="mobile-view"/>
    <div class="wrapper" id="desktop-view">
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
import MobileView from './components/MobileView.vue'
export default {
  name: 'App',

  components: {
    Logo,
    Welcome,
    LandingText,
    HeroCoverImg,
    EmailForm,
    MobileView,
  },
  
}
</script>

<style>
*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

.wrapper {
  font-size: 16px;
  background: gainsboro;
  display: flex;
  justify-content: center;
  align-items: center;
  width: 1000px;
  height: 500px;
  margin: 10rem 5rem;
  box-shadow:0 0 10px rgba(52, 51, 51, 0.8); 
  overflow: hidden;
}

.card{
  background-image: url(./assets/images/bg-pattern-desktop.svg),linear-gradient(135deg, hsl(0, 0%, 100%), hsl(0, 100%, 98%));
  display: flex;
  flex-direction: column;
  padding: 5rem;
  min-width: 55%;
}

#mobile-view {
  display:none;
}

@media screen and (max-width: 600px){
  
  #desktop-view {
    display: none;
}
#mobile-view {
  display: flex;
  flex-direction: column;
  width: 100%;
}

.mobile-btn{
  position: absolute;
  top: 21%;
  right: 0;

}
.mobile-arrow {
    position: absolute;
    top: 25%;
    right: 50%;
    bottom: 50%;
    left: 50%;
}
#btn-padding {
    display: flex;
    align-items: center;
    justify-content: center;
}
}



</style>
