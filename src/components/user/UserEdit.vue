<template>
  <div>
    <h3>Edit the User</h3>
    <hr />
    <p>Locale: {{ $route.query.locale }}</p>
    <p>Analytics: {{ $route.query.q }}</p>
    <button class="btn btn-primary" @click="confirmed = true">Confirm</button>
    <div style="height: 1200px"></div>
    <p id="data">Here is some additional data</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      confirmed: false
    };
  },
  beforeRouteEnter(to, from, next) {
    console.log("beforeRouteEnter");
    next();
  },
  beforeRouteLeave(to, from, next) {
    if (this.confirmed) {
      next();
    } else {
      if (confirm("Are you sure?")) {
        next();
      } else {
        next(false);
      }
    }
  }
};
</script>