<template>
  <input
    type="text"
    :value="value"
    @input="onChange"
    :placeholder="placeholder"
  />
</template>

<script>
export default {
  props: {
    value: String,
    placeholder: String,
  },
  methods: {
    onChange(e) {
      this.$emit("input", e.target.value);
    },
  },
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
