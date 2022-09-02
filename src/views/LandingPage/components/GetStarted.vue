<template>
  <div class="content">
    <div class="title">Boost your links today</div>
    <CustomeButton inputClass="primary">Get Started</CustomeButton>
  </div>
</template>

<script>
import CustomeButton from "../../../Element/CustomeButton.vue";
export default {
  components: { CustomeButton },
};
</script>

<style scoped>
.content {
  background-image: url("@/assets/bg-boost-desktop.svg");
  height: 300px;
  background-size: cover;
  background-color: var(--bg-color1);
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
}

.title {
  font-size: 40px;
  font-weight: bold;
  margin-bottom: 30px;
  color: white;
}
</style>
