<template>
    <v-app>
      <v-container>
        <v-menu>
          <template v-slot:activator="{ on, attrs }">
            <v-btn color="primary" dark v-bind="attrs" v-on="on">
              QUẢN TRỊ VIÊN
            </v-btn>
          </template>
          <v-list>
            <v-list-item>
              <v-list-item-title>Thông tin cá nhân</v-list-item-title>
            </v-list-item>
            <v-list-item>
              <v-list-item-title>Đổi mật khẩu</v-list-item-title>
            </v-list-item>
            <v-list-item>
              <v-list-item-title>Đăng xuất</v-list-item-title>
            </v-list-item>
          </v-list>
        </v-menu>
      </v-container>
    </v-app>
</template>
  
<script>
  export default {
    name: 'MenuComponent',
  };
</script>
  
<style scoped>
  .v-btn {
    border-radius: 8px;
  }
</style>
  