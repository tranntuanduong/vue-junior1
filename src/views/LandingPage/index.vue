<template>
  <div>
    <Banner />
    <ShortenLink />
    <AdvancedStatistics />
    <GetStarted />
    <Footer />
  </div>
</template>

<script>
import Banner from "../LandingPage/components/Banner.vue";
import ShortenLink from "../LandingPage/components/ShortenLink.vue";
import Container from "../../layout/Container.vue";
import AdvancedStatistics from "./components/AdvancedStatistics.vue";
import GetStarted from "./components/GetStarted.vue";
import Footer from "../../components/Footer.vue";
export default {
  components: {
    Banner,
    Container,
    ShortenLink,
    AdvancedStatistics,
    GetStarted,
    Footer,
  },
};
</script>
