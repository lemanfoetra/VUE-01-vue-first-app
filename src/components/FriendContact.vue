<template>
  <li>
    <h2>{{ name }} {{ isFavorite ? '(Favorite)' : '' }}</h2>
    <button @click="toggleIsFavorite">(Favorite)</button>
    <button @click="toggleDetails">
      {{ detailAreVisible ? "Hide" : "Show" }} Details
    </button>
    <button @click="$emit('delete-contact', id)">
      Delete
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
    id: {
      type: String,
      required: true,
    },
    name: {
      type: String,
      required: true,
      default: '-',
    },
    phoneNumber: {
      type: String,
      required: true,
    },
    emailAddress: {
      type: String,
      required: true,
      default: '-',
    },
    isFavorite: {
      type: Boolean,
      required: false,
      default: false,
    },
  },
  emits: [
    'favorite-event'
  ],
  data() {
    return {
      detailAreVisible: false,
    };
  },
  methods: {
    toggleDetails() {
      this.detailAreVisible = !this.detailAreVisible;
    },
    toggleIsFavorite() {
      this.$emit('favorite-event', this.id)
    },
  },
};
</script>
