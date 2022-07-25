<script setup lang="ts">
    import HistoryItem from './HistoryItem.vue'
</script>

<template>
    <div class="biddingHistory">
        <h5>Bidding History:</h5>
        <HistoryItem></HistoryItem>
        <HistoryItem></HistoryItem>
    </div>
</template>

<style lang="sass" scoped>
    .biddingHistory
        border-top: 1px #DDD solid
        margin-top: 10px
        padding-top: 10px
        h5
            margin-bottom: 10px
</style>