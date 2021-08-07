<template>
  <div id="Demo7">
    <h1>Demo7: Slot</h1>
    <Clock>
      <span style="color:red">เวลาปัจจุบัน</span>
    </Clock>
    <Clock>
      <span style="color:green">Date Now</span>
    </Clock>
    <Clock />
    <Clock>
      <template v-slot:header>
        <h1>Header</h1>
      </template>
      <span style="color:orange">เวลาปัจจุบัน</span>
      <template v-slot:footer>
        <h3>Footer</h3>
      </template>
    </Clock>
  </div>
</template>

<script>
import Clock from "../components/helper/Clock.vue";
export default {
  name: "Demo7",
  components: {
    Clock,
  },
};
</script>

<style></style>
