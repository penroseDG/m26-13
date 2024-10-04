<template>
    <div>
      <v-btn color="primary" @click="dialog = true">Xác nhận</v-btn>
      <v-dialog v-model="dialog" max-width="500px">
        <v-card>
          <v-card-title class="headline">
            <v-icon>mdi-refresh</v-icon>
            Xác nhận
          </v-card-title>
          <v-card-text>
            Bạn có xác nhận làm mới dữ liệu không? Nếu có dữ liệu sẽ được cập nhật.
          </v-card-text>
          <v-card-actions>
            <v-spacer></v-spacer>
            <v-btn color="primary" @click="dialog = false">Hủy</v-btn>
            <v-btn color="primary" @click="confirmRefresh">Xác nhận</v-btn>
          </v-card-actions>
        </v-card>
      </v-dialog>
    </div>
</template>
  
<script>
  export default {
    data() {
      return {
        dialog: false,
      };
    },
    methods: {
      confirmRefresh() {
        // Thực hiện hành động làm mới dữ liệu
        this.dialog = false;
      },
    },
  };
</script>
  
<style scoped>
  .headline {
    display: flex;
    align-items: center;
  }
  .headline v-icon {
    margin-right: 8px;
  }
</style>
  