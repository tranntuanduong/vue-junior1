<template>
  <div class="header">
    <div class="header__wrap">
      <div class="header__left">
        <div class="logo">
          <img alt="Vue logo" class="logo" src="@/assets/logo.svg" />
        </div>
        <div class="menu">
          <div class="menu__item">{{ mode }}</div>
          <div class="menu__item">Features</div>
          <div class="menu__item">Pricing</div>
          <div class="menu__item">Resources</div>
        </div>
      </div>

      <div class="header__right">
        <CustomeButton>Login</CustomeButton>
        <CustomeButton inputClass="primary">Sign up</CustomeButton>
      </div>
    </div>
  </div>
</template>

<script>
import CustomeButton from "../Element/CustomeButton.vue";

export default {
  name: "Header",
  components: {
    CustomeButton,
  },
  props: ["mode"],
};
</script>

<style>
.header {
  display: flex;
  justify-content: center;
  padding: 30px 16px;
  font-size: 16px;
  background-color: #fff;
}

.header__wrap {
  display: flex;
  width: 100%;
  max-width: 1200px;
  justify-content: space-between;
  align-items: center;
}

.header__left {
  display: flex;
}

.menu {
  display: flex;
  align-items: center;
  color: var(--text-grey);
  font-weight: 500;
  margin-left: 0px;
}

.menu__item {
  padding: 8px 16px;
  cursor: pointer;
}

.menu__item:hover {
  color: #3a393e;
}

.logo {
  height: 30px;
  cursor: pointer;
}

.header__right {
  display: flex;
}
</style>
