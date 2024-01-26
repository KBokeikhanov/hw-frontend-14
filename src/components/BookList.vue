

<template>
    <div>
      <h2>Books:</h2>
      <ul>
        <li v-for="(book, index) in books" :key="index">{{ book }}</li>
      </ul>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      books: Array,
    },
  };
  </script>
  
  <style scoped>
  </style>
  