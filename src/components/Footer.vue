<template>
  <div class="footer">
    <Container>
      <div class="footer-grid">
        <div class="logo">
          <img alt="Vue logo" class="logo__img" src="@/assets/logo.svg" />
        </div>
        <div class="column">
          <div class="title">Features</div>
          <div class="item">Link shortening</div>
          <div class="item">Branded Links</div>
          <div class="item">Analytics</div>
        </div>
        <div class="column">
          <div class="title">Resources</div>
          <div class="item">Blog</div>
          <div class="item">Developers</div>
          <div class="item">Support</div>
        </div>
        <div class="column">
          <div class="title">Company</div>
          <div class="item">About</div>
          <div class="item">Out Team</div>
          <div class="item">Careers</div>
          <div class="item">Support</div>
        </div>
        <div class="social">
          <img
            alt="Vue logo"
            class="social__img"
            src="@/assets/icon-facebook.svg"
          />
          <img
            alt="Vue logo"
            class="social__img"
            src="@/assets/icon-instagram.svg"
          />
          <img
            alt="Vue logo"
            class="social__img"
            src="@/assets/icon-pinterest.svg"
          />
          <img
            alt="Vue logo"
            class="social__img"
            src="@/assets/icon-twitter.svg"
          />
        </div>
      </div>
    </Container>
  </div>
</template>

<script>
import Container from "../layout/Container.vue";
export default { components: { Container } };
</script>

<style scoped>
.footer {
  padding: 30px 0;
  background-color: var(--bg-color3);
  color: white;
}

.logo__img {
  filter: invert(100%) sepia(29%) saturate(0%) hue-rotate(38deg)
    brightness(104%) contrast(101%);
}

.logo {
  grid-column: 2 span;
}

.title {
  font-weight: bold;
  margin-bottom: 30px;
}

.item {
  color: var(--text-grey);
  cursor: pointer;
}

.item:hover {
  color: var(--primary-color1);
}

.item + .item {
  margin-top: 10px;
}

.social {
  display: flex;
  column-gap: 15px;
  justify-content: center;
}

.social .social__img {
  width: 30px;
  height: 30px;
  object-fit: cover;
}

.footer-grid {
  display: grid;
}

@media (min-width: 0px) {
  .footer-grid {
    grid-template-columns: repeat(1, 1fr);
  }
  .logo {
    grid-column: 1;
    margin: auto;
  }

  .column {
    text-align: center;
    margin-top: 40px;
  }

  .social {
    margin: auto;
    margin-top: 30px;
  }
}
@media (min-width: 655px) {
  .footer-grid {
    grid-template-columns: repeat(6, 1fr);
  }
}
@media (min-width: 1300px) {
  .footer-grid {
    grid-template-columns: repeat(6, 1fr);
  }
}
</style>
