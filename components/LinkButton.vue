<template>
  <NuxtLink :to="`/${Text}`" class="link-text">
    <div class="link-button">{{ Text }}</div>
  </NuxtLink>
</template>

<script setup>
const props = defineProps(["Text"]);
</script>

<style lang="scss" scoped>
$mainColor: #a490cd;
$subColor: #d2cdf6;
$thirdColor: #c59fce;
$textColor: #fff;

.link-button {
  width: 200px;
  height: 80px;
  background: transparent;
  border-radius: 30px;
  border: 1px solid $textColor;
  font-size: 25px;
  color: $textColor;
  cursor: pointer;
  text-align: center;
  line-height: 81px;
  box-sizing: border-box;

  &:hover {
    background: $textColor;
    color: $mainColor;
  }
}

.link-text {
  text-decoration: none;
  &:hover {
    color: $mainColor;
  }
}
</style>
