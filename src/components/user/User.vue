<template>
  <div>
    <h1>The User Page</h1>
    <hr />
    <p>Loaded id: {{ id }}</p>
    <hr />
    <button class="btn btn-primary" @click="navigateToTome">Go to home</button>
  </div>
</template>

<script>
export default {
  props: ["id"],
  methods: {
    navigateToTome() {
      this.$router.push("/");
    }
  }
};
</script>