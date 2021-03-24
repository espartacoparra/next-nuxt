<template>
  <div>a</div>
</template>

<script>
export default {
  name: "user",
  data() {
    return {
      users: [],
    };
  },
  methods: {
    async getUsers() {
      const ip = await this.$axios.$get(
        "https://jsonplaceholder.typicode.com/users"
      );
      console.log(ip);
      this.ip = ip;
    },
  },
  created() {
    this.getUsers();
  },
};
</script>

<style lang="scss" scoped>
</style>