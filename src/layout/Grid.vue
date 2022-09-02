<template>
  <div class="grid">
    <slot></slot>
  </div>
</template>

<style scope>
.grid {
  display: grid;
  grid-template-columns: repeat(3, auto);
  justify-content: center;
  row-gap: 40px;
  column-gap: 40px;
}

@media (min-width: 0px) {
  .grid {
    grid-template-columns: repeat(1, auto);
  }
}
@media (min-width: 655px) {
  .grid {
    grid-template-columns: repeat(1, auto);
  }
}
@media (min-width: 1300px) {
  .grid {
    grid-template-columns: repeat(3, auto);
  }
}
</style>
