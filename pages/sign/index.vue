<template>
  <div class="sign_wrap">
    <back-button />

    <h1 class="title">Sign Up</h1>

    <div class="input_wrap">
      <user-input v-model="id" :placeholder="placeId" />
      <user-input v-model="password" :placeholder="placePw" />
      <user-input v-model="passwordCheck" :placeholder="placePwCheck" />
      <user-input v-model="nickName" :placeholder="placeNickName" />
    </div>

    <confirm-button :button-text="confirm" :id="id" :pw="password" />

    <div class="login_button">
      <NuxtLink to="/Login" class="link_login">
        <span>Login</span>
      </NuxtLink>
    </div>
  </div>
</template>

<script setup>
import BackButton from "../../components/BackButton.vue";
import ConfirmButton from "../../components/ConfirmButton.vue";
import UserInput from "../../components/UserInput.vue";

import { ref } from "vue";

const confirm = ref("Sign Up");
const id = ref("");
const password = ref("");
const passwordCheck = ref("");
const nickName = ref("");
const placeId = ref("ID");
const placePw = ref("Password");
const placePwCheck = ref("Password Check");
const placeNickName = ref("NickName");
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
