<template>
  <div class="intro_wrap">
    <div class="button_div">
      <LinkButton :Text="login" />
      <LinkButton :Text="signUp" />
    </div>
  </div>
</template>

<script>
import LinkButton from "../components/LinkButton.vue";
export default {
  components: {
    LinkButton,
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
