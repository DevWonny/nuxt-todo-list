<template>
  <div class="intro_wrap">
    <Button :Text="login" @click="onClick" />
    <Button :Text="signUp" @click="onClick" />
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
      signUp: "Sign Up",
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
.intro_wrap {
  max-width: 500px;
  height: 100vh;
  margin: auto;
  display: flex;
}
</style>
