<template>
  <div>
    <!-- <h2>Xin chào {{ $route.params.id }}</h2> -->
    <input type="text" v-model="userId" />
    <button @click="onLoadUser">Load User</button>
    <nuxt-child />
  </div>
</template>
<script>
export default {
  data() {
    return {
      userId: "",
    };
  },
  methods: {
    onLoadUser() {
      this.$router.push("/users/" + this.userId);
    },
  },
  layout: 'users',
};
</script>

<style scoped></style>
