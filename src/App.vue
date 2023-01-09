<template>
  <MsHeader></MsHeader>
  <div class="d-flex align-items-center">
    <MsSideBar></MsSideBar>
    <MsContent></MsContent>
  </div>
</template>

<script>
import MsHeader from "./components/layouts/MsHeader.vue";
import MsSideBar from "./components/layouts/MsSideBar.vue";
import MsContent from "./components/layouts/MsContent.vue";
export default {
  components: { MsHeader, MsSideBar, MsContent },
};
</script>

<style lang="scss">
@import "./assets/sass/main.scss";
</style>
