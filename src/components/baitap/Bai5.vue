<template>
    <v-dialog v-model="dialog" max-width="500px">
      <v-card>
        <v-card-title class="headline">
          Xác nhận
          <v-spacer></v-spacer>
          <v-btn icon @click="dialog = false">
            <v-icon>mdi-close</v-icon>
          </v-btn>
        </v-card-title>
        <v-card-text>
          Bạn có chắc chắn muốn xóa tài khoản này không?
        </v-card-text>
        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn color="primary" text @click="dialog = false">Hủy</v-btn>
          <v-btn color="primary" @click="confirmDelete">Xác nhận</v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
</template>
  
<script>
  export default {
    data() {
      return {
        dialog: false,
      };
    },
    methods: {
      confirmDelete() {
        // Thực hiện hành động xóa tài khoản
        this.dialog = false;
      },
    },
  };
</script>
  
<style scoped>
  .headline {
    font-weight: bold;
  }
</style>
  