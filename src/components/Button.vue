<template>
  <div id="register">
    <input
      type="button"
      value="Register"
      class="button-register"
    /> <a href="../views/SucessView.vue"></a>
  </div>
</template>

<script>
export default {
  name: "Button",
};
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

</style>
