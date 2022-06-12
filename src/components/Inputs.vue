<template>
  <div id="form">
    <div class="form1">
      <label for="fullname">Full Name *</label>
      <input
        type="text"
        autocomplete="nope"
        required
        class="input1"
        placeholder="Name"
        id="nameInput"
      />
      <span id="span0" class="clear">Fullname invalid</span>
    </div>
    <div class="form2">
      <label for="email">Email *</label>
      <input
        type="email"
        autocomplete="nope"
        required
        class="input2"
        placeholder="foo@bar.com"
        id="emailInput"
      />
      <span id="span1" class="clear">Email invalid</span>
    </div>
    <div class="form3">
      <label for="phone">Phone *</label>
      <input
        type="tel"
        required
        autocomplete="nope"
        placeholder="(83) 00000-0000"
        class="input3"
        id="phoneInput"
      />
      <span id="span2" class="clear">Phone invalid</span>
    </div>

    <div class="form4">
      <label for="password">Password *</label>
      <input
        type="password"
        required
        autocomplete="nope"
        class="input4"
        id="passwordInput"
        placeholder="Enter your password"
      />
      <span id="span3" class="clear">Password invalid</span>
    </div>
    <div class="form5">
      <label for="birthday">Birthday *</label>
      <input
        type="date"
        required
        placeholder="yyyy/mm/dd"
        class="input5"
        id="birthdayInput"
      />
      <span id="span4" class="clear">Birthday invalid</span>
    </div>
  </div>
</template>

<script>
export default {
  name: "Inputs",
};
</script>

<style scooped>
#form {
  display: flex;
  flex-flow: row wrap;
  margin: 3vh 0vw;
  color: #767676;
}

#form .form1 {
  width: 100%;
}

#form .form2,
#form .form4 {
  width: 65%;
}

#form .form1,
#form .form2 {
  padding-bottom: 4vw;
}

#form .form3,
#form .form5{
  width: 35%;
  padding-left: 3vw;
}

#form input {
  margin: 0 auto;
  display: block;
  border: 2px solid #aaaaaa;
  border-radius: 4px;
  height: 3em;
  background: white;
  padding: 0 10px;
  color: #767676
}

#form input:focus {
  outline: 0;
}

.input1 {
  width: 100%;
}

.input2,
.input4 {
  width: 100%;
}

.input3,
.input5 {
  width: 100%;
}

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


</style>
