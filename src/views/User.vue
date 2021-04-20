<template>
  <div>
    <h1>Welcome {{user}}</h1>
    <button @click="logOut" class="btn">Log Out</button>
  </div>
</template>

<script>
import store from "@/store";
export default {
  data() {
    return {
      user: store.user
    };
  },
  name: "user",
  methods: {
    logOut() {
      store.user = null;
      this.$router.push("/");
    }
  }
};
</script>

<style scoped>

</style>