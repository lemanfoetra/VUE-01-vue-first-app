<template>
  <li>
    <h2>{{ name }}</h2>
    <button @click="toggleDetails">
      {{ detailAreVisible ? "Hide" : "Show" }} Details
    </button>
    <ul v-if="detailAreVisible">
      <li><strong>Phone : </strong> {{ phoneNumber }}</li>
      <li><strong>Email : </strong>{{ emailAddress }}</li>
    </ul>
  </li>
</template>

<script>
export default {
  props: ["name", "phoneNumber", "emailAddress"],
  data() {
    return {
      detailAreVisible: false,
      friend: {
        id: 1,
        name: "Manuel Lorenz",
        phone: "0857937468",
        email: "manuesl@mail.com",
      },
    };
  },
  methods: {
    toggleDetails() {
      this.detailAreVisible = !this.detailAreVisible;
    },
  },
};
</script>
