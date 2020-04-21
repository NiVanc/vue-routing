<template>
  <div>
    <h3>Edit the User</h3>
    <hr />
    <p>Locale: {{ $route.query.locale }}</p>
    <p>Analytics: {{ $route.query.q }}</p>
    <div style="height: 1200px"></div>
    <p id="data">Here is some additional data</p>
  </div>
</template>

<script>
export default {
  beforeRouteEnter(to, from, next) {
    console.log("beforeRouteEnter");
    next();
  }
};
</script>