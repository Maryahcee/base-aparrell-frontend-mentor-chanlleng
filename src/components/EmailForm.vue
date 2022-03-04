<template>
<div class="email">
  <input v-model="address" placeholder="Email Adress">
  <button class="click">
          <img :src="icon">
      </button>
</div>
</template>

<script>
import icon from  '../assets/images/icon-arrow.svg'
 
export default {
    name: 'Form',
    name: 'icon',

    props: ({ 
        Form:'',
        icon: '',
    }),

  data: function() {
    return{
      address:'',
      icon:'',
    }
  }
}
</script>

<style>
input {
    padding: 13px;
    height: 28px;
    border-radius: 15px;
    border-style: none;
}
.click {
    background-color:hsl(0, 36%, 70%);
    padding: 3px;
    margin: -19px;
    border-radius: 30px;
    width: 50px;
    height: 28px;
    border-style: none;
}
</style>