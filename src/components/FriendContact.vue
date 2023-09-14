<template>
  <li>
    <h2>{{ friend.name }}</h2>
    <button @click="toggleDetails">
      {{ detailAreVisible ? "Hide" : "Show" }} Details
    </button>
    <ul v-if="detailAreVisible">
      <li><strong>Phone : </strong> {{ friend.phone }}</li>
      <li><strong>Email : </strong>{{ friend.email }}</li>
    </ul>
  </li>
</template>

<script>
export default {
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
