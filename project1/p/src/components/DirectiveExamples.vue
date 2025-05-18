<template>
  <div>
    <!-- <h1 v-if="isLoggedIn">Welcome back, user!</h1> -->
    <h1 v-show="isLoggedIn">Welcome back, user!</h1>
    <!-- <h1 v-else-if="count < 5">Condition is true!</h1>
    <h1 v-else>Please log in to continue.</h1> -->

    <!-- <button @click="toggleLogin">
      {{ isLoggedIn ? 'Logout' : 'Login' }}
    </button> -->
    <ul>
        <li v-for="(item, index) in arr" :key="index">
            {{ index + 1 }}. {{ item }}
        </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isLoggedIn: false,
      count:  10,
      arr:["one", "Two", "Three", "Four", "Five"],
    };
  },
  methods: {
    // toggleLogin() {
    //   this.isLoggedIn = !this.isLoggedIn;
    // }
  }
};
</script>
