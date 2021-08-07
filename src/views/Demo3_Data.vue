<template>
  <div>
    <h1>Demo3: Data</h1>
    <div>{{ count }}</div>
    <button @click="count += 1">Count++</button>
    <div>{{ message }}</div>
    <div>{{ isLogged }}</div>
    <input type="text" placeholder="Enter a message" v-model="message" />
    <h2 v-if="isLogged">Yahoo</h2>
    <div>{{ account }}</div>
    <ul>
      <li v-for="(item, index) in courses" :key="index">{{ item }}</li>
    </ul>
    <span class="title">Eiei</span>
  </div>
</template>

<script>
export default {
  name: "Demo3",
  mounted() {
    this.message = "Welcome to Demo3";
  },
  data() {
    return {
      count: 0,
      message: "",
      isLogged: true,
      account: {
        username: "admin",
        password: "1234",
      },
      courses: ["Angular", "VueJS", "ReactiveJS"],
    };
  },
};
</script>

<style scoped>
li {
  color: red;
}
</style>
