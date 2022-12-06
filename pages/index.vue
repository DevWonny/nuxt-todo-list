<template>
  <div class="intro_wrap">
    <div class="button_div">
      <link-button :Text="login" />
      <link-button :Text="signUp" />
    </div>
  </div>
</template>

<script setup>
import LinkButton from "../components/LinkButton.vue";

const login = "Login";
const signUp = "Sign";
</script>

<style lang="scss">
$mainColor: #a490cd;
$subColor: #d2cdf6;
$thirdColor: #c59fce;
$textColor: #fff;

.intro_wrap {
  height: 100%;
  display: flex;
  align-items: center;
}

.button_div {
  width: 100%;
  height: 240px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
}
</style>
