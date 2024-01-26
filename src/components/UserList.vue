<!-- src/components/UserList.vue -->

<template>
    <div>
      <h2>Users:</h2>
      <ul>
        <li v-for="(user, index) in users" :key="index">
          {{ user.name }} has {{ user.books }} books
        </li>
      </ul>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      users: Array,
    },
  };
  </script>
  
  <style scoped>
  </style>
  