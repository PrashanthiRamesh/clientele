<template>
  <v-container class="my-5">
    <h1 class="grey--text pb-5">Clients</h1>
    <v-container class="my-5">
      <v-card>
        <v-card-title>
          <v-text-field
            v-model="search"
            append-icon="mdi-magnify"
            label="Search"
            single-line
            hide-details
          ></v-text-field>
        </v-card-title>
        <v-data-table
          :headers="headers"
          :items="clients"
          :search="search"
        ></v-data-table>
      </v-card>
    </v-container>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      search: "",
      clients: [
        {
          firstName: "Jon",
          lastName: "Snow",
          company: "GOT",
          phone: "4589653254",
          email: "jon.snow@gmail.com",
          address: "32 The Wall",
        },
        {
          firstName: "Wonder",
          lastName: "Women",
          company: "DC",
          phone: "4452589654",
          email: "wonder.women@gmail.com",
          address: "9 The Amazon",
        },
        {
          firstName: "Black",
          lastName: "Widow",
          company: "Marvel",
          phone: "5148569547",
          email: "black.widow@gmail.com",
          address: "4 The Red Room",
        },
        {
          firstName: "Arya",
          lastName: "Stark",
          company: "GOT",
          phone: "5412563258",
          email: "arya.stark@gmail.com",
          address: "67 The Sea",
        },
      ],
    };
  },
  computed: {
    headers() {
      return [
        {
          text: "First Name",
          value: "firstName",
        },
        {
          text: "Last Name",
          value: "lastName",
        },
        { text: "Company", value: "company" },
        { text: "Phone", value: "phone" },
        { text: "Email", value: "email" },
        { text: "Address", value: "address" },
      ];
    },
  },
};
</script>