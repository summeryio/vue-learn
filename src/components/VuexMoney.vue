<template>
  <div class="vuex-example">
    vuex-example-money
    {{ $store.state.money.money }}

    <button @click="add(10)">增加</button>
    <button @click="reduce">删减</button>
  </div>
</template>

<script>
import {mapActions} from 'vuex'
export default {
    methods: mapActions('money', ['add', 'reduce'])
}
</script>