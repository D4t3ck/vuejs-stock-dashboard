<template>
  <div class="card">
    
  </div>
</template>

<script>
export default {
  name: "BaseCard",
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/mixins.scss";

.card {
  @include randomBorder;
  background: var(--cardColor);
  border-radius: 16px;
  padding: 24px 32px;
  width: 1240px;
}
</style>
