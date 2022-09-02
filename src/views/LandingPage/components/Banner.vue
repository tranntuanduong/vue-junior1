<template>
  <div class="banner">
    <Container>
      <div class="content">
        <div class="title">More than just shorter links</div>
        <div class="desc">
          Build your brand's recognition and get detailed insights on how your
          links are performing
        </div>
        <CustomeButton inputClass="primary">Get Started</CustomeButton>
      </div>
    </Container>
    <div class="banner-img">
      <img src="@/assets/illustration-working.svg" alt="" class="img" />
    </div>
  </div>
</template>

<script>
import CustomeButton from "../../../Element/CustomeButton.vue";
import Container from "../../../layout/Container.vue";
export default {
  components: {
    CustomeButton,
    Container,
  },
};
</script>

<style scoped>
.banner {
  width: 100%;
  position: relative;
  padding-bottom: 160px;
  background-color: #fff;
}

.banner-img {
  position: absolute;
  right: 0;
  top: 30px;
  width: 100%;
  max-width: 550px;
  transform: translateX(60px);
  z-index: 1;
}

.img {
  width: 100%;
  aspect-ratio: 1.52074688797;
  -webkit-user-drag: none;
}

.content {
  max-width: 600px;
  margin-left: 20px;
  position: relative;
  z-index: 2;
}
.title {
  font-size: 80px;
  font-weight: bold;
  letter-spacing: -3px;
  margin-top: 30px;
}

.desc {
  color: var(--text-grey);
  font-weight: 500;
  line-height: 1.4;
  margin-top: 8px;
  margin-bottom: 30px;
  text-shadow: 2px 2px #c5c5c53b;
}

@media (min-width: 0px) {
  .content{
    margin-top: 400px;
    text-align: center;
    display: flex;
    flex-direction: column;
    align-items: center;
  }
 
}
@media (min-width: 655px) {

}
@media (min-width: 1300px) {
  
}
</style>
