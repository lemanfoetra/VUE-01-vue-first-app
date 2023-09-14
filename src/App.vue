<template>
  <section>
    <header>
      <h1>My Freinds</h1>
    </header>
    <ul>
      <friend-contact></friend-contact>
      <friend-contact></friend-contact>
      <friend-contactxx></friend-contactxx>
      <friend-contactxx></friend-contactxx>
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