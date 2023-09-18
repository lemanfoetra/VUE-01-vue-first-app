<template>
  <section>
    <header>
      <h1>My Freinds</h1>
    </header>
    <ul>
      <friend-contact
        v-for="friend in friends"
        :key="friend.id"
        :name="friend.name"
        :phone-number="friend.phone"
        :email-address="friend.email"
      >
      </friend-contact>
    </ul>
  </section>
</template>

<script>
export default {
  data() {
    return {
      friends: [
        {
          id: 1,
          name: "Manuel Lorenz",
          phone: "0857937468",
          email: "manuesl@mail.com",
        },
        {
          id: 2,
          name: "Manuel Lorenz 2",
          phone: "0857937468",
          email: "manuesl@mail.com",
        },
        {
          id: 3,
          name: "Manuel Lorenz 3",
          phone: "0857937468",
          email: "manuesl@mail.com",
        },
      ],
    };
  },
};
</script>

<style>
@import url("./styles/styles.css");
</style>