<template>
  <div>
    <p v-if="user.isLoggedIn">Welcome back, {{ user.name }}!</p>
    <p v-else>Purchased Watch</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      user: {
        isLoggedIn: false,
        name: 'Alice'
      }
    };
  }
};
</script>