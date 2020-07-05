<template>
  <div class="home">
    <img alt="Vue logo" src="@/assets/logo.png">
    <HelloWorld 
      :count="count"
      @handleCount="handleCount"
    >
      <h1 slot="a">slot a</h1>
      <h1 slot="b">slot b</h1>
    </HelloWorld>

    <!-- vuex -->
    <VuexMoney />
    <VuexCount />
  </div>
</template>

<script>
import HelloWorld from '@/components/HelloWorld.vue'
import VuexMoney from '@/components/VuexMoney.vue'
import VuexCount from '@/components/VuexCount.vue'

export default {
  name: 'home',
  components: {
    HelloWorld,
    VuexMoney, 
    VuexCount
  },
  data: () => {
    return {
      count: 1000
    }
  },
  methods: {
    handleCount: function (user) {
      console.log(user);
      
      this.count++
    }
  },
}
</script>
