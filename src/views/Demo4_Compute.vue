<template>
  <div id="demo4">
    <h1>Demo4: Compute</h1>
    <h2>{{ fullname }}</h2>
  </div>
</template>

<script>
export default {
  name: "Demo4",
  methods: {
    getrandomno1: function() {
      return Math.random();
    },
  },
  data() {
    return {
      firstname: "Thanawat",
      lastname: "Phutchips",
    };
  },
  computed: {
    fullname() {
      return this.firstname + " " + this.lastname;
    },
    getrandomno() {
      return Math.random();
    },
  },
};
</script>

<style></style>
