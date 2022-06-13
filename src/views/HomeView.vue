<template>
  <div class="home">
   <div id="logo">
     <img src="../img/data1.png" alt="">
   </div> 
   <h1 id="title">Intern Sign Up</h1>
  <Inputs/>
  <div id="footer">
    <Checkbox/>
   <Button/>
  </div>



  </div>
</template>

<script>
import Inputs from '../components/Inputs.vue'
import Checkbox from '../components/Checkbox.vue'
import Button from '../components/Button.vue'


export default {
  name: 'Home',
  components: {
    Inputs,
    Checkbox,
    Button
  }
}
</script>

<style scooped>
.home {
  max-width: 620px;
  height: 100%;
  margin: 0 auto;
  background: white;
}

#logo {
  display: flex;
  justify-content: center;
  padding-top: 5vh;
}

#title {
  font-family: "Inter", sans-serif;
  line-height: 1.5em;
  font-size: 2.25em;
  margin-top: 10px;
  color: #111111;
  text-align: center;
}

#footer {
  display: flex;
  justify-content: space-between;
  padding: 10vh 0;

}

span {
  display: block;
}

.warning {
  color: red;
  display: visible;
  padding: 5px 0px 0px 5px;
  font-size: 1em;
}

.clear {
  display: block;
  /* visibility: hidden; */
  padding-left: 5px;
  font-size: 1em;
  padding-top: 5px;
}

@media (max-width: 768px){
#footer {
    margin: 0 auto;
    display: flex;
    flex-flow: column wrap;
    padding: 15px 0;
  }
  
  #title {
    margin: 5px;
  }

}

@media (max-height:750px) {


  #logo {
    padding-top: 10px;
  }

  #footer {
    padding: 10px 0;
  }
}

</style>
