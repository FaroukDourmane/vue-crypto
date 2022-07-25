<script setup lang="ts">
    import {ref, reactive} from 'vue';
    

    let bidType = reactive({type: "buy"});
    let bidObject = ref({
        limit: null,
        price: null,
        amount: null,
        type: bidType
    });
    
    let bids = reactive([]);
    
    const addBid = () => {
      bids.push(bidObject.value);
      bidObject.value = {
        limit: null,
        price: null,
        amount: null,
        type: bidType
      }      
    }

    const switchBid = (type) => {
        bidType.type = type;
        // bidObject.value.type = bidType.value;
    }

    const activeClass = (type) => {        
        return bidType.type == type
    }

</script>

<template>
    <form action="" @submit.prevent="addBid()">
        <div class="switchBox">
            <div :class="{'buy': true, active: activeClass('buy')}" @click="switchBid('buy')">Buy</div>
            <div :class="{'sell': true, active: activeClass('sell')}" @click="switchBid('sell')">Sell</div>
        </div>        
        <div>
            <h2>BTC/USDT</h2>
            <div class="label">
                <input type="number" v-model="bidObject.limit" name="" id="" placeholder="limit" />
            </div>
            <div class="label">
                <input type="number" v-model="bidObject.price" name="" id="" placeholder="Price" />
                <input type="number" v-model="bidObject.amount" name="" id="" placeholder="Amount" />
            </div>
            <button>{{bidType.type}}</button>
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
            cursor: pointer
        .buy            
            color: darken(green, 20)
            border-radius: 10px 0 0 10px
            &.active
                background: lighten(green , 10)
                color: #FFF
        .sell            
            border-radius: 0 10px 10px 0
            color: darken(red, 20)
            &.active
                background: darken(red , 14)
                color: #FFF
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