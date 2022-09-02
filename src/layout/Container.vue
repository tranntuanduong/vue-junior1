<template>
  <div :class="`container ${classList}`">
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: "Container",
  components: {},
  props: ["classList"],
};
</script>

<style scope>
.container {
  max-width: 1248px;
  margin-left: auto;
  margin-right: auto;
  padding: 30px 16px;
}

.mt-20 {
  margin-top: 20px;
}
</style>
