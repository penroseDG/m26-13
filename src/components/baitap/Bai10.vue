<template>
    <v-container>
      <v-card>
        <v-card-title>Item</v-card-title>
        <v-card-text>
          <v-data-table
            :headers="headers"
            :items="items"
            item-value="name"
            class="elevation-1"
          >
            <template v-slot:item="{ item }">
              <v-chip
                :color="getStatusColor(item.status)"
                dark
                small
              >
                {{ item.status }}
              </v-chip>
            </template>
          </v-data-table>
  
          <v-row class="mt-3">
            <v-col cols="12" sm="6">
              <v-select
                v-model="itemsPerPage"
                :items="itemsPerPageOptions"
                label="Items per page"
                dense
                outlined
              ></v-select>
            </v-col>
            <v-col cols="12" sm="6" class="text-right">
              <v-pagination
                v-model="page"
                :length="totalPages"
                total-visible="7"
              ></v-pagination>
            </v-col>
          </v-row>
        </v-card-text>
      </v-card>
    </v-container>
</template>
  
<script>
  export default {
    data() {
      return {
        headers: [
          { text: 'Name', value: 'name' },
          { text: 'Project Name', value: 'project' },
          { text: 'Post', value: 'post' },
          { text: 'Status', value: 'status' },
          { text: 'Budget', value: 'budget', align: 'right' }
        ],
        items: [
          {
            name: 'Sunil Joshi',
            project: 'Elite Admin',
            post: 'Web Designer',
            status: 'Active',
            budget: '$3.9'
          },
          {
            name: 'Andrew McDownland',
            project: 'Real Homes WP Theme',
            post: 'Project Manager',
            status: 'Pending',
            budget: '$24.5k'
          },
          {
            name: 'Christopher Jamil',
            project: 'MedicalPro WP Theme',
            post: 'Project Manager',
            status: 'Completed',
            budget: '$12.8k'
          },
          {
            name: 'Nirav Joshi',
            project: 'Hosting Press HTML',
            post: 'Frontend Engineer',
            status: 'Active',
            budget: '$2.4k'
          },
          {
            name: 'Micheal Doe',
            project: 'Helping Hands WP Theme',
            post: 'Content Writer',
            status: 'Cancel',
            budget: '$9.3k'
          }
        ],
        page: 1,
        itemsPerPage: 5,
        itemsPerPageOptions: [5, 10, 15],
        totalPages: 2
      };
    },
    methods: {
      getStatusColor(status) {
        switch (status) {
          case 'Active':
            return 'green lighten-2';
          case 'Pending':
            return 'orange lighten-2';
          case 'Completed':
            return 'blue lighten-2';
          case 'Cancel':
            return 'red lighten-2';
          default:
            return 'grey lighten-2';
        }
      }
    }
  };
</script>
  
<style scoped>
  .v-chip {
    font-weight: bold;
  }
</style>
  