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
.email {
    position: relative;
    margin-top: 2.5rem;
    height: 3rem;
}

input {
    padding: 13px;
    height: 28px;
    border-radius: 2rem;
    border: 1px solid var(--red-light);
    color: var(--red-light);
    padding: 0.2rem 1.5rem;
    height: 2.4rem;
    width: 50%;
}

input::placeholder {
  color: var(--red-light);
}

input:focus,
button:focus {
  outline: none;
}

button {
 background: linear-gradient(90deg, hsl(0, 80%, 86%), hsl(0, 74%, 74%));
 border: 0;
 border-radius: 2rem;
 box-shadow: 0 5px 20px 3px hsl(0, 80%, 86%);
 position: absolute;
 top: 0;
 right: 50%;
 width: 5rem;
 height: 80%;
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