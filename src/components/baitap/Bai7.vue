<template>
    <v-pagination
      v-model="page"
      :length="totalPages"
      circle
    ></v-pagination>
</template>
  
<script>
  export default {
    data() {
      return {
        page: 1,
        totalPages: 4, // Số trang bạn muốn hiển thị
      };
    },
  };
</script>
  
<style scoped>
  .v-pagination {
    justify-content: center;
  }
</style>
  