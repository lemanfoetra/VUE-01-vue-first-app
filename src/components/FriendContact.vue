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
  // props: ["name", "phoneNumber", "emailAddress"],
  props: {
    name: {
      type: String,
      required: true,
      default : '-',
    },
    phoneNumber : {
      type : String,
      required : true,
    },
    emailAddress : {
      type : String,
      required : true,
      default : '-',
    },
  },
  data() {
    return {
      detailAreVisible: false,
    };
  },
  methods: {
    toggleDetails() {
      this.detailAreVisible = !this.detailAreVisible;
    },
  },
};
</script>
