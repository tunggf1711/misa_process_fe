<template>
  <div class="sidebar">
    <div
      :class="['sidebar__item', index === itemActivedIndex ? 'active' : '']"
      v-for="(item, index) of SIDEBAR_ITEM"
      :key="index"
      @click="activeSidebarItem(index)"
    >
      <MsIcon
        :iconColor="index === itemActivedIndex ? 'blue' : 'grey'"
        iconFile="iconProcess"
        iconSize="s-24"
        :iconStyle="item.iconStyle"
      ></MsIcon>
      {{ item.title }}
    </div>
  </div>
</template>

<script>
import { SIDEBAR_ITEM } from "@/resources/resources";
import MsIcon from "../base/MsIcon.vue";
export default {
  data() {
    return {
      SIDEBAR_ITEM,
      itemActivedIndex: -1,
    };
  },
  methods: {
    activeSidebarItem(index) {
      this.itemActivedIndex = index;
    },
  },
  components: { MsIcon },
};
</script>

<style lang="scss">
@import "./../../assets/sass/layouts/sidebar.scss";
</style>
