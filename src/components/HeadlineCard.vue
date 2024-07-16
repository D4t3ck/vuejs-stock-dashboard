<template>
  <div class="headline_card">
    <img src="../../public/images/head_deco.png" />
    <h1>{{ headline }}</h1>
  </div>
</template>

<script>
export default {
  name: "HeadlineCard",

  data() {
    return {
      headline: "The Magnificent Seven Companies",
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/mixins.scss";

.headline_card {
  @include randomBorder;
  @include flexbox($jc: unset, $g: 1.5rem);
  position: absolute;
  top: 4rem;
  left: 0;
  height: 43px;

  h1 {
    margin: 0;
  }
}
</style>
