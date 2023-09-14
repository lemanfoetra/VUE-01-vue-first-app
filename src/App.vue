<template>
  <section>
    <header>
      <h1>My Freinds</h1>
    </header>
    <ul>
      <friend-contact
        name="Ardyn Sulaeman"
        phone-number="085793647568"
        email-address="ardyn.sulaeman@gmail.com"
      >
      </friend-contact>
      <friend-contact-two
        name="Ai Inka Agustina"
        phone-number="085127838488"
        email-address="inka@gmail.com"
      ></friend-contact-two>
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
          id: 2,
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