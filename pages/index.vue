<template>
  <div class="intro_wrap">
    <div class="button_div">
      <Button :Text="login" />
      <Button :Text="signUp" />
    </div>
  </div>
</template>

<script>
import Button from "../components/Button.vue";
export default {
  components: {
    Button,
  },
  data() {
    return {
      login: "Login",
      signUp: "Sign",
    };
  },
  methods: {
    onClick(item) {
      console.log(`${item} 페이지로 이동!`);
    },
  },
};
</script>

<style lang="scss">
$mainColor: #a490cd;
$subColor: #d2cdf6;
$thirdColor: #c59fce;
$textColor: #fff;

.intro_wrap {
  max-width: 500px;
  height: 100vh;
  margin: auto;
  background: linear-gradient(45deg, $mainColor, $thirdColor);
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
