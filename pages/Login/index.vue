<template>
  <div class="login_wrap">
    <h1 class="title">Login</h1>
    <div class="input_div">
      <UserInput v-model="id" :placeholder="placeId"></UserInput>
      <UserInput v-model="password" :placeholder="placePw"></UserInput>
    </div>

    <div class="confirm_div">
      <ConfirmButton
        :button-text="confirm"
        :id="id"
        :pw="password"
      ></ConfirmButton>
    </div>
  </div>
</template>

<script>
import UserInput from "~/components/UserInput.vue";
import ConfirmButton from "../../components/ConfirmButton.vue";

export default {
  components: {
    UserInput,
    ConfirmButton,
  },
  data() {
    return {
      id: "",
      password: "",
      placeId: "ID",
      placePw: "Password",
      confirm: "Login",
    };
  },
};
</script>

<style lang="scss" scoped>
.login_wrap {
  height: 100%;

  .input_div {
    width: 90%;
    height: 180px;
    margin-left: 5%;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }
}
</style>
