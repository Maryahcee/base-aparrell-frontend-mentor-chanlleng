<template>
<div class="email">

   <form action="" @submit.prevent="submitForm">
          <span v-if="!validEmail(address)">
            <img class="icon-error" src="../assets/images/icon-error.svg" alt="">
          </span>

          <input class="input-info" v-model="address"  type="email" placeholder="Email Adress" required >

      <button @click="submitForm" class="click">
          <img :src="icon"  class="arrow">
      </button>
      <div>
        <span class="error-message"  v-if="!validEmail(address) ">
          {{error}} </span>
      </div>
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
     error: 'Please provide a valid email address',
    }
  },
  methods: {
    submitForm() {
      console.log()
    },
    validEmail: function (email) {
      if (email == ""){
        return true;
      }
      var re = /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/;
      return re.test(email);
    },
  
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
  margin-top: 2rem;
  height: 2.5rem;
  width: 50rem;
}

.input-info {
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
  box-shadow: 0 5px 15px 4px hsl(0, 80%, 86%);
  position: absolute;
  top: 0;
  right: 50%;
  width: 5rem;
  height: 98%;
  cursor: pointer;
  border-style: none;
  transition:0.4s ;
}

.click:hover {
  background: linear-gradient(45deg, hsl(0, 70%, 67%), hsl(0, 77%, 78%)); 

}
.arrow {
   width: 10px;
   justify-content: center;
   align-content: center;
   margin: 2px 0;
}

.error-message {
  color: hsl(0, 93%, 68%);
  font-style: italic;
  padding: 20px;
  margin-top: 1rem ;
}

.icon-error {
  position: absolute;
  padding: 6px;
  margin-left: 17rem;
}


</style>