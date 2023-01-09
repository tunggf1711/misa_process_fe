<template>
  <div class="header">
    <div class="header__left">
      <div class="box-app-menu"></div>
      <div class="app__logo mr-34">{{ APP_NAME }}</div>
      <div class="navbar">
        <div
          class="navbar__item"
          v-for="(item, index) of NAVBAR_ITEM_TITLE"
          :key="index"
        >
          {{ item }}
        </div>
      </div>
      <MsIcon
        iconColor="grey"
        iconFile="iconControl"
        iconSize="s-24"
        iconStyle="three-dot"
        class="mr-20"
      ></MsIcon>
      <MsButton color="blue">
        <div class="button__content">
          <MsIcon
            iconColor="white"
            iconSize="s-20"
            iconFile="iconProcess"
            iconStyle="run-process"
          ></MsIcon>
          {{ BUTTON_TITLE.RUN_PROCESS }}
        </div>
      </MsButton>
    </div>
    <div class="header__right">
      <div class="input__container mr-8">
        <MsIcon
          iconColor="light-grey"
          iconFile="iconControl"
          iconSize="s-24"
          iconStyle="search"
        ></MsIcon>
        <input type="text" placeholder="Tìm kiếm" />
      </div>
      <div class="header__tools">
        <div class="notification"></div>
        <MsIcon
          iconColor="grey"
          iconFile="iconProcess"
          iconSize="s-24"
          iconStyle="questions"
          class="mr-8"
        ></MsIcon>
        <MsIcon
          iconColor="grey"
          iconFile="iconProcess"
          iconSize="s-24"
          iconStyle="option-extend"
        ></MsIcon>
      </div>
      <div class="user__avatar">
        <img
          src="https://testcdnamisapp.misacdn.net/APIS/PlatformAPI/api/Avatar/5a426d1d-f731-4d88-962f-52b7756868ba/594LXLY7.jpg?avatarID=a1015034-89ce-45db-b1e4-cca57d9eb281&width=64&height=64&v=20211108"
          alt=""
        />
      </div>
    </div>
  </div>
</template>

<script>
import {
  APP_NAME,
  NAVBAR_ITEM_TITLE,
  BUTTON_TITLE,
} from "@/resources/resources";
import MsIcon from "../base/MsIcon.vue";
import MsButton from "../base/MsButton.vue";
export default {
  data() {
    return {
      APP_NAME,
      NAVBAR_ITEM_TITLE,
      BUTTON_TITLE,
    };
  },
  components: { MsIcon, MsButton },
};
</script>

<style lang="scss">
@import "./../../assets/sass/layouts/header.scss";
@import "./../../assets/sass/base/icon.scss";
</style>
