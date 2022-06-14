<template>
  <div class="home">
    <div id="logo">
      <img src="../img/data1.png" alt="" />
    </div>
    <h1 id="title">Intern Sign Up</h1>
    <div class="formFull">
      <Inputs
        placeholderInput="Full name"
        typeInput="text"
        classInput="formName"
        labelInput="name"
        idInput="Fullname"
        v-model="name"
        classForm="formNameFull"
        classLabel="label1"
      />
      <Inputs
        placeholderInput="Email"
        typeInput="text"
        classInput="formEmail"
        labelInput="email"
        idInput="Email"
        v-model="email"
        classForm="formEmailFull"
        classLabel="label2"
      />
      <Inputs
        placeholderInput="Phone"
        typeInput="phone"
        classInput="formPhone"
        labelInput="phone"
        idInput="Phone"
        v-model="phone"
        classForm="formPhoneFull"
        classLabel="label3"
      />
      <Inputs
        placeholderInput="Password"
        typeInput="password"
        classInput="formPw"
        labelInput="password"
        idInput="Password"
        v-model="password"
        classForm="formPwFull"
        classLabel="label4"
      />
      <Inputs
        typeInput="date"
        classInput="formBirth"
        labelInput="birthday"
        idInput="Birthday"
        v-model="birthday"
        classForm="formBirthFull"
        classLabel="label5"
      />
    </div>

    <div id="footer">
      <Checkbox />
      <ButtonRegister @click="register"/>
    </div>
  </div>
</template>

<script>
import Inputs from "../components/Inputs.vue";
import Checkbox from "../components/Checkbox.vue";
import ButtonRegister from "../components/ButtonRegister.vue";

export default {
  name: "Home",
  components: {
    Inputs,
    Checkbox,
    ButtonRegister,
    name: "",
    email: "",
    password: "",
    phone: "",
    birthday: "",
  },
  data() {
    return {
      formName: "formName",
      formEmail: "formEmail",
      formPhone: "formPhone",
      formPw: "formPw",
      formName: "formBirth",
    };
  },
  methods: {
    caio() {
      console.log(this.name);
    },

    register() {
      console.log("funcionou");
    },
  },
};
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

.formFull {
  display: flex;
  flex-flow: row wrap;
  margin: 3vh 0vw;
  color: #767676;
}

.formFull .formNameFull {
  width: 100%;
}

.formFull .formEmailFull,
.formFull .formPwFull {
  width: 60%;
}

.formFull .formNameFull,
.formFull .formEmailFull {
  padding-bottom: 20px;
}

.formFull .formPhoneFull,
.formFull .formBirthFull {
  width: 40%;
  padding-left: 3vw;
}

.formFull input {
  margin: 0 auto;
  display: block;
  border: 2px solid #aaaaaa;
  border-radius: 4px;
  height: 3em;
  background: white;
  padding: 0 10px;
  color: #767676;
}

.formFull input:focus {
  outline: 0;
}

.formName,
.formEmail,
.formPhone,
.formPw,
.formBirth {
  width: 100%;
}

#footer {
  display: flex;
  justify-content: space-between;
  padding: 10vh 0;
}

span {
  display: block;
}

small {
  color: red;
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

@media (max-width: 768px) {
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

@media (max-height: 750px) {
  #logo {
    padding-top: 10px;
  }

  #footer {
    padding: 10px 0;
  }
}
</style>
