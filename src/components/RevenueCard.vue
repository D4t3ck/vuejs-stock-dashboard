<template>
  <div class="card_container"></div>
</template>

<script>
export default {
  name: "RevenueCard",
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/mixins.scss";

.card_container {
  @include randomBorder;
  width: 1240px;
  padding: 24px 32px;
  background: var(--cardColor);
  border-radius: 16px;
}
</style>
