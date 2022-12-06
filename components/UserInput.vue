<template>
  <input
    type="text"
    :value="value"
    @input="onChange"
    :placeholder="placeholder"
  />
</template>

<script setup>
const props = defineProps(["value", "placeholder"]);

const emit = defineEmits("input");

const onChange = (e) => {
  emit("input", e.target.value);
};
</script>

<style lang="scss" scoped>
input {
  width: 100%;
  height: 60px;
  border: none;
  border-radius: 10px;
  outline: none;
  font-size: 20px;
}
</style>
