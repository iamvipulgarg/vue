<template>
  <!-- <ul>
    <li>
      <a href="">Home</a>
      <a href="">Product</a>
      <a href="">Gallery</a>
      <a href="">Contact</a>
      <a href="">About Us</a>
    </li>
  </ul> -->

  <button @click="increment">Increment</button>
  <button @click="decrement">Decrement</button>
  <h3>{{ counter }}</h3>
</template>

<script>
export default {
    // For data binding or states management
  data() {
    return {
      counter: 0
    }
  },
  methods: {
    increment() {
      this.counter++
    },
    decrement() {
      this.counter--
    }
  }
}
</script>

<style scoped>
a {
  text-decoration: none;
  margin-left: 10px;
  font-size: 18px;
  font-weight: bold;
}
</style>
