<template>
  <div class="box-terms">
    <label class="terms">
      <input
        type="checkbox"
        name="terms"
        checked
        value="xD"
        class="chk"
        id="checkbox"
        required
      />
      <span class="geekmark"></span>
      <span class="label-text">I accept the terms and privacy</span>
    </label>
    <small id="small5" class="clear">You must accept the terms</small>
  </div>
</template>

<script>
export default {
  name: "Checkbox",
};
</script>

<style scooped>

/* Checkbox stlying */
input[type="checkbox"] {
  visibility: hidden;
}

.terms {
  display: block;
  position: relative;
  cursor: pointer;
  
}
.geekmark {
  position: absolute;
  top: 9px;
  left: 5px;
  height: 18px;
  width: 18px;
  background-color: white;
  border: solid 2px #0dbdbd;
  box-shadow: 1px 1px 1px rgba(0, 0, 0, 0.5);
}

.terms input:checked ~ .geekmark {
  background-color: #0dbdbd;
}


.geekmark:after {
  content: "";
  position: absolute;
  display: none;
}

.terms input:checked ~ .geekmark:after {
  display: block;
}

.terms .geekmark:after {
  left: 5px;
  bottom: 1px;
  width: 2.5px;
  height: 10px;
  border: solid white;
  border-width: 0 3px 5px 0;
  -webkit-transform: rotate(45deg);
  -ms-transform: rotate(45deg);
  transform: rotate(45deg);
}


.box-terms label {
  color: #111111;
  cursor: pointer;
  display: flex;
  font-size: 1.125em;
  padding-left: 20px;
  padding-top: 10px;
  text-shadow: 0.5px 0.5px 10px rgb(0, 0, 0, 0.5);
}


</style>
