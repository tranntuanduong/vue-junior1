<template>
  <Container>
    <div class="content">
      <div class="top">
        <div class="title">Advanced Statistics</div>
        <div class="desc">
          Track how your links are performing across the web with our advanced
          statistics dashboard.
        </div>
      </div>
      <Grid>
        <StatisticCard />
        <StatisticCard :classList="'card-2 divider'" />
        <StatisticCard :classList="'card-3'" />
      </Grid>
    </div>
  </Container>
</template>

<script>
import Container from "../../../layout/Container.vue";
import Grid from "../../../layout/Grid.vue";
import StatisticCard from "./StatisticCard.vue";
export default {
  components: {
    Container,
    Grid,
    StatisticCard,
  },
};
</script>

<style scoped>
.content {
  margin-top: 60px;
}

.title {
  font-size: 40px;
  font-weight: bold;
  text-align: center;
}

.desc {
  text-align: center;
  font-size: 20px;
  color: var(--text-grey);
  margin-top: 25px;
  max-width: 600px;
  line-height: 1.5;
}

.top {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding-bottom: 120px;
}
</style>
