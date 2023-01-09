<template>
  <button :class="['button', color]"><slot></slot></button>
</template>

<script>
export default {
  props: ["color"],
};
</script>

<style lang="scss">
@import "./../../assets/sass/base/button.scss";
</style>
