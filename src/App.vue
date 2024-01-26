<!-- src/App.vue -->

<template>
  <div>
    <h1>{{ msg }}</h1>
    <book-list :books="books" />
    <user-list :users="users" />
    <div>
      <button @click="incrementCounter">Increment</button>
      <button @click="decrementCounter">Decrement</button>
      <p v-show="showLimitReached" style="color: red;">Limit reached!</p>
      <p>{{ count }}</p>
    </div>
  </div>
</template>

<script>
import BookList from "./components/BookList.vue";
import UserList from "./components/UserList.vue";

export default {
  data() {
    return {
      msg: "Test message",
      count: 0,
      showLimitReached: false,
      books: ["Book1", "Book2", "Book3"],
      users: [
        {
          name: "User1",
          age: 23,
          books: 3,
        },
        {
          name: "User2",
          age: 15,
          books: 6,
        },
        {
          name: "User3",
          age: 40,
          books: 5,
        },
      ],
    };
  },
  methods: {
    incrementCounter() {
      if (this.count < 10) {
        this.count++;
        this.showLimitReached = false;
      } else {
        this.showLimitReached = true;
      }
    },
    decrementCounter() {
      if (this.count > -10) {
        this.count--;
        this.showLimitReached = false;
      } else {
        this.showLimitReached = true;
      }
    },
  },
  components: {
    BookList,
    UserList,
  },
};
</script>

<style>
/* Add your styles here */
</style>
