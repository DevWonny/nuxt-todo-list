<template>
  <div class="login_wrap">
    <h1 class="title">Login</h1>
    <div class="input_div">
      <UserInput></UserInput>
      <UserInput></UserInput>
    </div>
  </div>
</template>

<script>
import UserInput from "~/components/UserInput.vue";
export default {
  components: {
    UserInput,
  },
};
</script>

<style lang="scss" scoped>
.login_wrap {
  height: 100%;
}
</style>
