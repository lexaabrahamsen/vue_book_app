<template>
  <div class="home">
    <h1>All Books</h1>
    <div v-for="book in books">
      <h2>{{ book.name }}</h2>
      <p>Pages: {{ book.pages }}</p>
    </div>
  </div>
</template>

<style>
</style>

<script>
import axios from "axios";

export default {
  data: function() {
    return {
      books: []
    };
  },
  created: function() {},
  methods: {}
};
</script>