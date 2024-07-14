<template>
  <div>
    <HeadlineCard />
    <BaseCard />
  </div>
</template>

<script>
import BaseCard from "./components/BaseCard.vue";
import HeadlineCard from "./components/HeadlineCard.vue";
import { stockService } from "@/services/stockService";

export default {
  name: "App",
  components: {
    BaseCard,
    HeadlineCard,
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

body {
  margin: 0;
  max-width: 1920px;
  font-family: system-ui, sans-serif;
  box-sizing: border-box;
  user-select: none;
}

#Basecard{
  @include flexbox;
}

#app {
  position: relative;
  width: 100vw;
  height: 100vh;
  padding: 155px 100px;
  background: var(--backgroundColor);
  box-sizing: border-box;
  color: whitesmoke;
}
</style>
