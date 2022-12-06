<template>
  <div class="confirm_button_wrap">
    <button>{{ buttonText }}</button>
  </div>
</template>

<script setup>
const props = defineProps(["buttonText", "id", "pw"]);

// method -> 클릭 이벤트 필요
</script>

<style lang="scss" scoped>
$mainColor: #a490cd;
$subColor: #d2cdf6;
$thirdColor: #c59fce;
$textColor: #fff;

.confirm_button_wrap {
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;

  button {
    width: 70%;
    height: 50px;
    background: transparent;
    border: 1px solid $textColor;
    border-radius: 10px;
    box-sizing: border-box;
    color: $textColor;
    font-size: 20px;
    cursor: pointer;

    &:hover {
      background: $textColor;
      color: $mainColor;
    }
  }
}
</style>
