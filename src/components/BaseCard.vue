<template>
  <div class="card">
    <!-- Slot für beliebigen Inhalt -->
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: "BaseCard",
};
</script>

<style scoped>
.card {
  background: var(--cardColor);
  border-radius: 16px;
  padding: 24px 32px;
}
</style>
