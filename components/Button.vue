<template>
  <button @click="$emit('click', Text)">{{ Text }}</button>
</template>

<script>
export default {
  props: {
    Text: String,
  },
};
</script>

<style lang="scss" scoped>
button {
  width: 300px;
  height: 30px;
}
</style>
