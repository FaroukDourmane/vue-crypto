<script setup lang="ts">
</script>

<template>
    <div class="biddingHistoryItem">
        <div class="currency">ETH/BTC <span class="type buy">BUY</span></div>
        <div class="info">            
            <span>Price: <b>10$</b></span>
            <span>Amount: <b>0.123</b></span>
            <span>Limit: <b>0.123</b></span>
        </div>
        <div class="options">
            <a href="#" class="cancel">Cancel</a>
        </div>
    </div>
</template>

<style lang="sass" scoped>
    .biddingHistoryItem
        display: flex
        gap: 10px
        align-items: center
        background: #f9f9f9
        border: 1px #f1f1f1 solid
        padding: 10px
        border-radius: 10px
        margin-bottom: 10px
        &:last-child
            margin-bottom: 0
        .currency
            flex-shrink: 0
            font-weight: bold
            font-size: 20px
            border-right: 1px #DDD solid
            padding-right: 10px
            span
                display: block
                font-size: 12px
                font-weight: bold
                border-radius: 5px
                text-align: center
                &.buy
                    background: rgba(green, 0.2)
                    color: darken(green, 10)
                &.sell
                    background: rgba(red, 0.2)
                    color: darken(red, 10)
        .info
            width: 100%
            span
                display: block
                font-size: 13px
                b
                    font-size: 15px
                    font-weight: bold
        .options
            flex-shrink: 0
            a
                display: inline-block
                line-height: 35px
                padding: 0 10px
                background: rgba(red, 0.1)
                color: darken(red, 10)
                text-decoration: none
                border-radius: 5px
                transition: .3s
                &:hover
                    background: rgba(red, 0.7)
                    color: #FFF
</style>