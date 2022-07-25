<script setup lang="ts">
    import CurrencyItem from './CurrencyItem.vue';
    import { onMounted } from 'vue';
    import axios from 'axios';
    import {reactive} from 'vue';

    let data = reactive([]);

    onMounted(() => {
        axios
            .get('https://api2.binance.com/api/v3/ticker/24hr')
            .then( response => {
                data.push(...response.data);                
            } )
    });
</script>

<template>
    <div class="currenciesBox">
        <CurrencyItem v-for="item in data.slice(0, 5)" v-bind:key="item.symbol">
            <template #currency>{{item.symbol}}</template>
            <template #priceChangePercent>{{item.priceChangePercent}}%</template>
            <template #volume>{{item.volume}}</template>
            <template #lastPrice>{{item.lastPrice}}$</template>
        </CurrencyItem>
    </div>
</template>

<style scoped>
    .currenciesBox{
        border: 1px #f1f1f1 solid;
        padding: 10px;
        border-radius: 10px;        
    }
</style>