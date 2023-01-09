<template>
  <div :class="[iconStyle, iconFile, iconSize, iconColor, 'icon']"></div>
</template>

<script>
export default {
  props: ["iconStyle", "iconFile", "iconSize", "iconColor"],
};
</script>

<style lang="scss">
@import "./../../assets/sass/base/icon.scss";
</style>
