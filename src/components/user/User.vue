<template>
  <div>
    <h1>The User Page</h1>
    <hr />
    <button class="btn btn-primary" @click="navigateToTome">Go to home</button>
  </div>
</template>

<script>
export default {
  methods: {
    navigateToTome() {
      this.$router.push("/");
    }
  }
};
</script>