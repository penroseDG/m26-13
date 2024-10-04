<template>
    <v-container>
      <v-row>
        <!-- Basic Layout Form -->
        <v-col cols="12" md="6">
          <v-card>
            <v-card-title>Basic Layout</v-card-title>
            <v-card-text>
              <v-form>
                <v-text-field label="Name" value="John Deo"></v-text-field>
                <v-text-field label="Company" value="ACME Inc."></v-text-field>
                <v-text-field label="Email" value="john.deo"></v-text-field>
                <v-text-field label="Phone No" value="412 2150 451"></v-text-field>
                <v-textarea label="Message" value="Hi, Do you have a moment to talk Jeo?"></v-textarea>
                <v-btn color="primary">Send</v-btn>
              </v-form>
            </v-card-text>
          </v-card>
        </v-col>
  
        <!-- Basic with Icons Form -->
        <v-col cols="12" md="6">
          <v-card>
            <v-card-title>Basic with Icons</v-card-title>
            <v-card-text>
              <v-form>
                <v-text-field
                  label="Name"
                  prepend-inner-icon="mdi-account"
                  value="John Deo"
                ></v-text-field>
                <v-text-field
                  label="Company"
                  prepend-inner-icon="mdi-office-building"
                  value="ACME Inc."
                ></v-text-field>
                <v-text-field
                  label="Email"
                  prepend-inner-icon="mdi-email"
                  value="john.deo"
                ></v-text-field>
                <v-text-field
                  label="Phone No"
                  prepend-inner-icon="mdi-phone"
                  value="412 2150 451"
                ></v-text-field>
                <v-textarea
                  label="Message"
                  prepend-inner-icon="mdi-message"
                  value="Hi, Do you have a moment to talk Jeo?"
                ></v-textarea>
                <v-btn color="primary">Send</v-btn>
              </v-form>
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
</template>
  
<script>
  export default {
    name: 'ContactForm',
  };
</script>
  
<style scoped>
  .v-card {
    margin-bottom: 20px;
  }
</style>
  