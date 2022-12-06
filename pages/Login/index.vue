<template>
  <div class="login_wrap">
    <back-button />
    <h1 class="title">Login</h1>
    <div class="input_div">
      <user-input v-model="id" :placeholder="placeId"></user-input>
      <user-input v-model="password" :placeholder="placePw"></user-input>
    </div>

    <confirm-button
      :button-text="confirm"
      :id="id"
      :pw="password"
    ></confirm-button>

    <div class="sign_button">
      <NuxtLink to="/Sign" class="link_text">
        <span>Sign Up</span>
      </NuxtLink>
    </div>
  </div>
</template>

<script setup>
import UserInput from "~/components/UserInput.vue";
import ConfirmButton from "../../components/ConfirmButton.vue";
import BackButton from "../../components/BackButton.vue";

import { ref } from "vue";

const id = ref("");
const password = ref("");
const placeId = ref("ID");
const placePw = ref("Password");
const confirm = ref("Login");
</script>

<style lang="scss" scoped>
$mainColor: #a490cd;
$subColor: #d2cdf6;
$thirdColor: #c59fce;
$textColor: #fff;
.login_wrap {
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  position: relative;

  .title {
    text-align: center;
    color: $textColor;
    margin: 0;
    position: relative;
    top: -50px;
  }
  .input_div {
    width: 90%;
    height: 180px;
    margin-left: 5%;
    margin-bottom: 50px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }

  .link_text {
    text-decoration: none;
  }
  .sign_button {
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
