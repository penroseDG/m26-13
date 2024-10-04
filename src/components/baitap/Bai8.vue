<template>
    <v-app>
      <v-tabs v-model="activeTab" background-color="primary" dark>
        <v-tab>TRANG CHỦ</v-tab>
        <v-tab>GIỚI THIỆU</v-tab>
        <v-tab>LIÊN HỆ</v-tab>
      </v-tabs>
  
      <v-tabs-items v-model="activeTab">
        <v-tab-item>
          <v-card flat>
            <v-card-text>Tab trang chủ</v-card-text>
          </v-card>
        </v-tab-item>
        <v-tab-item>
          <v-card flat>
            <v-card-text>Tab giới thiệu</v-card-text>
          </v-card>
        </v-tab-item>
        <v-tab-item>
          <v-card flat>
            <v-card-text>Tab liên hệ</v-card-text>
          </v-card>
        </v-tab-item>
      </v-tabs-items>
    </v-app>
</template>
  
<script>
  export default {
    data() {
      return {
        activeTab: 0,
      };
    },
  };
</script>
  
<style></style>
  