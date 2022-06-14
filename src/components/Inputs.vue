<template>
  <div :class="classForm">
    <label :class="classLabel" :for="labelInput">{{ idInput }} *</label>
    <input
      :type="typeInput"
      required
      :class="classInput"
      :placeholder="placeholderInput"
      :id="idInput"
      :value="valueInput"
    />
    <small :id="small" class="clear">{{ idInput }} invalid</small>
  </div>
</template>

<script>




export function funcionando() {
  console.log("name");
}

export default {
  name: "Inputs",
  props: {
    placeholderInput:String,
    classInput:String,
    idInput:String,
    valueInput:String,
    labelInput:String,
    showInput:String,
    typeInput:String,
    classForm:String,
    classLabel:String,
    small:String,


  },
};
</script>

<style scooped>


input[type="date"]::-webkit-calendar-picker-indicator {
  color: #767676;
  opacity: 1;
  display: block;
  background: url(../img/vector.png) no-repeat;
  margin-top: 5px;
  width: 20px;
  height: 20px;
  border-width: thin;
}

@media (max-width: 768px) {
  #form {
    margin: 2vh auto;
  }

  #form .form1,
  #form .form2 {
    padding-bottom: 20px;
  }

  .form3,
  .form5 {
    order: 1;
  }

  .form2,
  .form4 {
    width: 100% !important;
  }

  .form3,
  .form5 {
    width: 50% !important;
    display: flex;
    flex-flow: column wrap;
    padding: 0px !important;
    margin-top: 2vh;
  }

  .input3,
  .input5 {
    display: flex !important;
    width: 95%;
  }

  .form5 {
    padding-right: 2vw;
    align-content: flex-end;
  }

  .input5 {
    justify-content: flex-end;
  }

  .input3 {
    margin: 0px !important;
    display: flex;
    justify-content: flex-start;
  }
}

@media (max-height: 750px) {
  #form {
    margin: 1vh auto;
  }

  #form .form1,
  #form .form2 {
    padding-bottom: 10px;
  }
}
</style>
