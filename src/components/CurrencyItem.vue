<script setup lang="ts">
</script>

<template>
    <div class="currencyItem">
        <div class="currency">
            <slot name="currency"></slot>
        </div>
        
        <div class="infos">
            <span>Change: <b><slot name="priceChangePercent"></slot></b></span>
            <span>Volume: <b><slot name="volume"></slot></b></span>
        </div>

        <div class="lastPrice"><slot name="lastPrice"></slot></div>
    </div>
</template>

<style lang="sass">
    .currencyItem
        width: 100%
        background: rgba(#f9f9f9, 0.3)
        box-shadow: 3px 3px 20px 0 rgba(0,0,0,0.05)
        margin-bottom: 10px
        border-radius: 10px
        display: flex
        gap: 10px
        align-items: center
        padding: 10px
        transition: 0.3s
        &:nth-child(even)
            background: #f9f9f9
        &:last-child
            margin-bottom: 0        
        .currency
            font-weight: bold
            flex-shrink: 0
            background: #f9f9f9
            padding: 10px
            border-radius: 10px
            transition: .3s ease-in-out
        .infos
            width: 100%
            span
                border-right: 1px #DDD solid
                padding-right: 10px
                margin-right: 10px
                color: #777
                b
                    font-weight: bold
                    color: #222
                &:last-child
                    border-right: none
        .lastPrice
            font-size: 17px
            flex-shrin: 0
            font-weight: bold
            color: green
        &:hover
            background: rgba(blue, 0.05)
            .currency
                background: rgba(blue, 0.1)
</style>