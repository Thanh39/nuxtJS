<template>
  <div>
    <h2>page {{ $route.params.id }}</h2>
  </div>
</template>

<script>
export default {
  // xác nhận xem trang đó có chạy không
  validate(data) {
    return /^\d+$/.test(data.params.id);
  },
  layout: 'users',
};
</script>

<style scoped></style>
