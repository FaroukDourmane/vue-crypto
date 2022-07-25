<script setup lang="ts">
    import Filters from './Filters.vue'
    import CurrenciesBox from './CurrenciesBox.vue'
    import BiddingForm from './BidingForm.vue'
    import BiddingHistory from './BiddingHistory.vue'
</script>

<template>
    <div class="home">
        <div class="listingsBox">
            <Filters />
            <CurrenciesBox />
        </div>

        <div class="biddingBox">
            <BiddingForm />
            <BiddingHistory />
        </div>        
    </div>
</template>

<style lang="sass" scoped>
    .home
        display: flex
        gap: 20px
        .listingsBox
            width: 100%
        .biddingBox
            width: 400px
            flex-shrink: 0
            box-shadow: -10px 0 25px 0 rgba(#000, 0.1)
            border-radius: 10px
            padding: 20px
</style>