<template>
  <div class="content__head">
    <div class="content__title">{{ CONTENT_TITLE }}</div>
    <MsButton color="blue">
      <div class="button__content">
        <MsIcon
          iconColor="white"
          iconFile="iconControl"
          iconSize="s-24"
          iconStyle="plus"
        ></MsIcon>
        {{ BUTTON_TITLE.ADD }}
      </div>
    </MsButton>
  </div>
</template>

<script>
import { CONTENT_TITLE, BUTTON_TITLE } from "@/resources/resources";
import MsButton from "../base/MsButton.vue";
import MsIcon from "../base/MsIcon.vue";
export default {
  data() {
    return {
      CONTENT_TITLE,
      BUTTON_TITLE,
    };
  },
  components: { MsButton, MsIcon },
};
</script>

<style lang="scss">
@import "./../../assets/sass/pages/user-group.scss";
</style>
