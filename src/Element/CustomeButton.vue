<template>
  <div class="btn" :class="inputClass">
    <slot></slot>
  </div>
</template>

<script>
export default {
  props: ["inputClass"],
};
</script>

<style scoped>
.btn {
  padding: 12px 28px;
  border-radius: 40px;
  font-weight: 500;
  color: var(--text-grey);
  cursor: pointer;
  width: fit-content;
  display: flex;
  align-items: center;
  justify-content: center;
}
.primary {
  background-color: var(--primary-color);
  color: white;
}

.primary1 {
  background-color: var(--primary-color1);
  color: white;
}

.primary1:hover {
  background-color: var(--primary-color);
}

.active {
  background-color: var(--bg-color1);
  color: white;
}

.active:hover {
  background-color: var(--bg-color2);
}

.minRadius {
  border-radius: 10px;
}
</style>
