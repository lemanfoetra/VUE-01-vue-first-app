<template>
  <section>
    <header>
      <h1>My Freinds</h1>
    </header>
    <new-friend-form @add-contact="addContact"></new-friend-form>
    <ul>
      <friend-contact v-for="friend in friends" :key="friend.id" :id="friend.id" :name="friend.name"
        :phone-number="friend.phone" :email-address="friend.email" :is-Favorite="friend.isFavorite"
        @favorite-event="favoriteEvent">
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
          isFavorite: false,
        },
        {
          id: 2,
          name: "Manuel Lorenz 2",
          phone: "0857937468",
          email: "manuesl@mail.com",
          isFavorite: true,
        },
        {
          id: 3,
          name: "Manuel Lorenz 3",
          phone: "0857937468",
          email: "manuesl@mail.com",
          isFavorite: false,
        },
      ],
    };
  },
  methods: {
    favoriteEvent(friendId) {
      let friend = this.friends.find((friend) => friend.id == friendId);
      friend.isFavorite = !friend.isFavorite
    },
    addContact(name, phone, email) {
      let newFriend = {
        id: (Math.random() * 1000000).toString(),
        name: name,
        phone: phone,
        email: email,
        isFavorite: false,
      }
      this.friends.push(newFriend)
    }
  }
};
</script>

<style>
@import url("./styles/styles.css");
</style>