<template>
<div class="email">

   <form action="">
          <input v-model="address" placeholder="Email Adress">
      <button class="click">
          <img :src="icon"  class="arrow">
      </button>
   </form>
</div>
</template>

<script>
import icon from  '../assets/images/icon-arrow.svg'
 
export default {
    name: 'Form',
    
    props: ({ 
        Form:'',
    }),

  data: function() {
    return{
      address:'',
     icon,
    }
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Josefin+Sans:ital,wght@0,300;0,400;0,600;1,300;1,400;1,600&display=swap');

*{
    --soft-red: hsl(0, 93%, 68%);
    --desaturated-red: hsl(0, 36%, 70%);
    --Dark-Grayish-Red: hsl(0, 6%, 24%);
}
.email {
    position: relative;
    margin-top: 3rem;
    height: 2.5rem;
    width: 50rem;
}

input {
    border-radius: 2rem;
    border: 1px solid var(--desaturated-red);
    color: var(--desaturated-red);
    padding: 0.2rem 1.5rem;
    height: 2.4rem;
    width: 25rem;
    font-family: "Josefin Sans";
    font-weight: 300;
}

input::placeholder {
  color: var(--red-light);
}

input:focus,
button:focus {
  outline: none;
}

.click {
 background: linear-gradient(90deg, hsl(0, 80%, 86%), hsl(0, 74%, 74%));
 border: 0;
 border-radius: 2rem;
 box-shadow: 0 5px 20px 3px hsl(0, 80%, 86%);
 position: absolute;
 top: 0;
 right: 50%;
 width: 5rem;
 height: 100%;
 cursor: pointer;
 border-style: none;
}

.arrow {
    width: 10px;
    justify-content: center;
    align-content: center;
    margin: 2px 0;
}
</style>