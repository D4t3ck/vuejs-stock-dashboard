<template>
  <main>
    <HeadlineCard />

    <section class="first_card">
      <BaseCard />
    </section>

    <section class="second_card">
      <RevenueCard />
    </section>

    <section class="third_card">
      <MiscDataCard />
    </section>
  </main>
</template>

<script>
import BaseCard from "./components/BaseCard.vue";
import HeadlineCard from "./components/HeadlineCard.vue";
import RevenueCard from "./components/RevenueCard.vue";
import MiscDataCard from "./components/MiscDataCard.vue";
import { stockService } from "@/services/stockService";

export default {
  name: "App",
  components: {
    BaseCard,
    HeadlineCard,
    RevenueCard,
    MiscDataCard,
  },
  async created() {
    this.data = await stockService.getRevenue("$AAPL");
    // console.log("Loaded data", this.data);
  },
};
</script>

<style lang="scss">
@import "./assets/scss/mixins.scss";

:root {
  --backgroundColor: radial-gradient(
    71.11% 100% at 50% 0%,
    #020204 14.6%,
    #011f35 100%
  );
  --cardColor: #011f35;
}

#app {
  position: relative;
  width: 100vw;
  max-width: 1920px;
  height: 100vh;
  padding: 155px 100px;
  background: var(--backgroundColor);
  box-sizing: border-box;
  color: whitesmoke;
}

body {
  @include flexbox;
  margin: 0;
  font-family: system-ui, sans-serif;
  box-sizing: border-box;
  user-select: none;
}

main {
  @include flexbox($fd: column, $g: 2rem);

  .first_card {
    @include flexbox;
  }

  .second_card {
    @include flexbox;
  }
}
</style>
