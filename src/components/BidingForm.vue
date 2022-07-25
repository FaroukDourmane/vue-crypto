<script setup lang="ts">
</script>

<template>
    <form action="">
        <div class="switchBox">
            <div class="buy">Buy</div>
            <div class="sell">Sell</div>
        </div>        
        <div>
            <h2>BTC/USDT</h2>
            <div class="label">
                <input type="number" name="" id="" placeholder="limit" />
            </div>
            <div class="label">
                <input type="number" name="" id="" placeholder="Price" />
                <input type="number" name="" id="" placeholder="Amount" />
            </div>            
            <button> Buy BTC </button>
        </div>        
    </form>
</template>

<style lang="sass" scoped>
    .switchBox
        display: flex
        justify-content: center
        margin-bottom: 20px
        .buy,.sell
            width: 50%
            text-align: center
            line-height: 45px
            font-weight: bold
            background: #DDD
        .buy
            background: lighten(green , 10)
            color: #FFF
            border-radius: 10px 0 0 10px
        .sell
            background: darken(red , 14)
            color: #FFF
            border-radius: 0 10px 10px 0
    form
        h2
            text-align: center
            margin-bottom: 10px
            border-bottom: 1px #f1f1f1 solid
            padding-bottom: 10px
        .label
            display: flex
            gap: 10px
            input
                width: 100%
                display: block
                line-height: 50px
                background: #f9f9f9
                font-weight: bold
                text-align: center
                width: 100%
                margin-bottom: 5px
                padding: 0 10px
                border: 0
                border-radius: 10px
        button
            display: block
            border: 0
            width: 100%
            text-align: center
            line-height: 50px
            margin-top: 10px
            border-radius: 10px
            cursor: pointer
            color: #FFF
            background: #222
            font-weight: bold
</style>