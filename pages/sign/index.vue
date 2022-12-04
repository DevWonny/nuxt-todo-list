<template>
  <div class="sign_wrap">
    <BackButton />

    <h1 class="title">Sign Up</h1>

    <div class="input_wrap">
      <UserInput v-model="id" :placeholder="placeId" />
      <UserInput v-model="password" :placeholder="placePw" />
      <UserInput v-model="passwordCheck" :placeholder="placePwCheck" />
      <UserInput v-model="nickName" :placeholder="placeNickName" />
    </div>

    <ConfirmButton :button-text="confirm" :id="id" :pw="password" />

    <div class="login_button">
      <NuxtLink to="/Login" class="link_login">
        <span>Login</span>
      </NuxtLink>
    </div>
  </div>
</template>

<script>
import BackButton from "../../components/BackButton.vue";
import ConfirmButton from "../../components/ConfirmButton.vue";
import UserInput from "../../components/UserInput.vue";

export default {
  components: {
    BackButton,
    ConfirmButton,
    UserInput,
  },

  data() {
    return {
      confirm: "Sign Up",
      id: "",
      password: "",
      passwordCheck: "",
      nickName: "",
      placeId: "ID",
      placePw: "Password",
      placePwCheck: "Password Check",
      placeNickName: "NickName",
    };
  },
};
</script>

<style lang="scss" scoped>
$mainColor: #a490cd;
$subColor: #d2cdf6;
$thirdColor: #c59fce;
$textColor: #fff;
.sign_wrap {
  height: 100%;
  position: relative;
  display: flex;
  flex-direction: column;
  justify-content: center;

  .title {
    text-align: center;
    color: $textColor;
    margin: 0;
    position: relative;
    top: -50px;
  }

  .input_wrap {
    width: 90%;
    height: 330px;
    margin-left: 5%;
    margin-bottom: 50px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }

  .link_login {
    text-decoration: none;
  }
  .login_button {
    margin: 0;
    height: 50px;
    text-align: center;
    position: relative;
    span {
      color: $textColor;
      cursor: pointer;
      line-height: 50px;
    }
  }
}
</style>
