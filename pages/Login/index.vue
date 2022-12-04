<template>
  <div class="login_wrap">
    <div><BackButton /></div>
    <h1 class="title">Login</h1>
    <div class="input_div">
      <UserInput v-model="id" :placeholder="placeId"></UserInput>
      <UserInput v-model="password" :placeholder="placePw"></UserInput>
    </div>

    <ConfirmButton
      :button-text="confirm"
      :id="id"
      :pw="password"
    ></ConfirmButton>

    <div class="sign_button">
      <NuxtLink to="/Sign" class="link-text">
        <span>회원가입</span>
      </NuxtLink>
    </div>
  </div>
</template>

<script>
import UserInput from "~/components/UserInput.vue";
import ConfirmButton from "../../components/ConfirmButton.vue";
import BackButton from "../../components/BackButton.vue";

export default {
  components: {
    UserInput,
    ConfirmButton,
    BackButton,
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

  .link-text {
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
