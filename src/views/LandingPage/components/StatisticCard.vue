<template>
  <div class="card-wrap" :class="classList">
    <div class="card">
      <div class="title">Brand Recognition</div>
      <div class="desc">
        Boost your brand recognition with each click. Generic links don't mean a
        thing. Branded links help insil confidence in your content.
      </div>
      <div class="logo">
        <img src="@/assets/icon-brand-recognition.svg" alt="" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["classList"],
};
</script>

<style scoped>
.card {
  padding: 40px 32px;
  background-color: white;
  box-shadow: var(--box-shadow-color) 0px 0.5rem 1rem 0px;
  min-width: 320px;
  border-radius: 10px;
  position: relative;
  height: fit-content;
  position: relative;
  z-index: 1;
}

.title {
  font-size: 22px;
  font-weight: bold;
  margin-top: 46px;
}

.desc {
  font-size: 16px;
  color: var(--text-grey);
  margin-top: 20px;
  line-height: 1.5;
}

.logo {
  position: absolute;
  width: 100px;
  height: 100px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: var(--bg-color2);
  top: 0;
  transform: translateY(-50%);
}

.card-wrap {
  position: relative;
}
.card-wrap.divider::after {
  position: absolute;
  content: "";
  background-color: var(--primary-color1);
  z-index: 0;
}

@media (min-width: 0px) {
  .card-wrap.divider::after {
    height: 500px;
    width: 8px;
    left: 50%;
    top: -100px;
    transform: translateX(-50%);
  }
  .logo {
    left: 50%;
    top: 0;
    transform: translate(-50%, -50%);
  }

  .card {
    text-align: center;
  }
  .card-2 {
    margin-top: 60px;
  }

  .card-3 {
    margin-top: 60px;
  }
}

@media (min-width: 1300px) {
  .card-wrap.divider::after {
    width: 500px;
    left: 200px;
    top: 110px;
    height: 8px;
  }

  .card-2 {
    margin-top: 50px;
  }

  .card-3 {
    margin-top: 100px;
  }
}
</style>
