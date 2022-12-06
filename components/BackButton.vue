<template>
  <div class="back_button" @click="onBack"></div>
</template>

<script setup>
const onBack = () => {
  window.history.go(-1);
};
</script>

<style lang="scss" scoped>
$mainColor: #a490cd;
$subColor: #d2cdf6;
$thirdColor: #c59fce;
$textColor: #fff;
.back_button {
  width: 50px;
  height: 50px;
  background-image: url("../assets/icon/Back_icon.svg");
  background-repeat: no-repeat;
  background-position: center;
  color: $textColor;
  position: absolute;
  top: 0;
  left: 0;
  cursor: pointer;
}
</style>
