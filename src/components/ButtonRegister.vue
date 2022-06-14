<template>
  <div id="register">
    <input
      type="button"
      value="Register"
      class="button-register"
    /> 
  </div>
</template>

<script>
import Inputs from './Inputs.vue'
import {funcionando} from './Inputs.vue'

export default {
  name: "Button",
  components: {
    Inputs,
  },
  methods: {
    sucessPage(){
      this.$router.push('Sucess');
    },
    
    funcionando

    

    }


  }



</script>

<style scooped>

.button-register {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  padding: 0px 12px;
  gap: 6px;
  width: 81px;
  height: 40px;
  background: #0dbdbd;
  color: white;
  border: none;
  border-radius: 10px;
  margin-right: 15px;
}

.button-register:hover {
  background: #0ca1a1;
  cursor: pointer;
}

@media (max-width:768px){

  .button-register {
    display: flex;
    justify-content: center;
    align-items: center;
    margin: 0 auto;
    width: 95%;
    height: 7vh;
    margin-top: 20px;
  }
}

</style>
