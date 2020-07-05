<template>
  <div class="hello">
    <slot name="a"></slot>
    
    <h1>{{ count }}</h1>
    <button @click="$emit('handleCount', {
        name: 'summer',
        age: 22
    })">btn</button>

    <slot name="b"></slot>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    count: Number
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss"></style>
