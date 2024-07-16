<template>
    <div class="revenue_card">
        
    </div>
</template>

<script>
export default {
    name: 'RevenueCard'
}
</script>

<style lang="scss" scoped>
@import "../assets/scss/mixins.scss";

.revenue_card {
    @include randomBorder;
    width: 1240px;
    padding: 24px 32px;
    background: var(--cardColor);
    border-radius: 16px;
}

</style>