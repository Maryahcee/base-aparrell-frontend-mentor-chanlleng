<template>
  <div v-show="!mobile" id="mobile-card">
        <div class="mobile-logo">
            <img :src="Logo">
        </div>
        <div  class="mobile-Img">
            <img :src="mobileImg" >
        </div>
        <div class="mobile-content">
            <h1 class="mobile-header">
                <span class="header-coloured">We're <br> </span>
        <span class="dark-color middle-header"> Coming <br> </span>
        <span class="dark-color"> Soon</span> 
            </h1>
            <p class="landing-mobile"> 
            Hello Fellow Shoppers! We're currrently building oour new fashion store.
        Add your email below to stay up-to-date with announcements and our launch deals.
            </p>
        </div>
        <div class="mobile-padding">
            <form  id="mobile-address">
                <input class="mobile-input" type="email" placeholder="Email Address">
                <button class="mobile-btn">
                    <img class="mobile-arrow" :src="arrow" alt="">
                </button>
            </form>
        </div>
  </div>
</template>

<script>
import Logo from '../assets/images/logo.svg'
import mobileImg from '../assets/images/hero-mobile.jpg'
import arrow from '../assets/images/icon-arrow.svg'
export default {
name: 'MobileView',
props: '',

data: function() {
return{
    Logo,
    mobileImg,
    arrow,
}
},

}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Josefin+Sans:ital,wght@0,300;0,400;0,600;1,300;1,400;1,600&display=swap');

*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
#mobile-card {
    background: linear-gradient(135deg, hsl(0, 0%, 100%), hsl(0, 100%, 98%));
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    
}

.mobile-logo {
    padding: 30px 0 30px 30px;
}

.mobile-Img {
    max-width: 100%;
    height: 100%;
}

.mobile-Img img {
    width: fill;
    padding-bottom: 30px;
}

.mobile-content {
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.mobile-header {
    text-transform: uppercase;
    font-family: 'Josefin Sans';
    font-weight: 600;
    line-height: 1.3;
    letter-spacing: 5px;
}

.header-coloured{
  color: hsl(0, 36%, 70%);
  line-height: 1.3;
  font-weight: 300;
}


.dark-color {
    color: hsl(0, 6%, 24%);
}

.landing-mobile{
    padding: 10px 25px;
    text-decoration: none;
    color: hsl(0, 36%, 70%);
    line-height: 1.4;
    font-size: 16px;
    font-family: 'Josefin Sans';
    font-weight: 400;
}

.mobile-input {
    border-radius: 2rem;
    border: 1px solid var(--desaturated-red);
    color: var(--desaturated-red);
    padding: 0.1rem 1.5rem;
    height: 3rem;
    width: 20rem;
    font-family: "Josefin Sans";
    font-weight: 300;
}

.mobile-btn {
 background: linear-gradient(90deg, hsl(0, 80%, 86%), hsl(0, 74%, 74%));
 border: 0;
 border-radius: 2rem;
 box-shadow: 0 5px 15px 4px hsl(0, 80%, 86%);
 position: absolute;
 top: 22%;
 right: 15%;
 width: 5rem;
 height: 3rem;
 cursor: pointer;
 border-style: none;
 transition:0.4s ;
}

.mobile-padding {
    padding: 20px 60px;
    position: relative;
}
</style>