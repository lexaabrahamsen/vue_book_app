  <template>
  <div class="container">
    <h1>All Books</h1>
    <div v-for="book in books">
      <h2>Title: {{ book.title }}</h2>
      <p>Pages: {{ book.pages }}</p>
    </div>
  </div>
</template>

<script>
import axios from "axios";

export default {
  data: function() {
    return {
      books: []
    };
  },
  created: function() {
    axios.get("/api/books").then(response => {
      this.books = response.data;
    });
  },
  methods: {}
};
</script>