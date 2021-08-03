<template>
  <v-dialog max-width="600px">
    <template v-slot:activator="{ on, attrs }">
      <v-btn v-bind="attrs" v-on="on" color="blue-grey" class="white--text"
        >Add new client</v-btn
      >
    </template>
    <v-card>
      <v-card-title>
        <div class="grey--text text--darken-2">Add a new client</div>
      </v-card-title>
      <v-card-text>
        <v-form class="px-3">
          <v-text-field
            label="First Name"
            v-model="firstName"
            prepend-icon="mdi-account"
          ></v-text-field>
          <v-text-field
            label="Last Name"
            v-model="lastName"
            prepend-icon="mdi-account"
          ></v-text-field>
          <v-text-field
            label="Company"
            v-model="company"
            prepend-icon="mdi-domain"
          ></v-text-field>
          <v-text-field
            label="Phone"
            v-model="phone"
            prepend-icon="mdi-phone"
          ></v-text-field>
          <v-text-field
            label="Address"
            v-model="address"
            prepend-icon="mdi-map-marker"
          ></v-text-field>
          <v-btn class="mt-4 green lighten-2 white--text" @click="submit"
            >Add Client</v-btn
          >
        </v-form>
      </v-card-text>
    </v-card>
  </v-dialog>
</template>

<script>
export default {
  data() {
    return {
      firstName: "",
      lastName: "",
      company: "",
      phone: "",
      address: "",
    };
  },
  methods: {
    submit() {
      console.log(this.firstName, this.address);
    },
  },
};
</script>