<template>
  <div class="book">
    <router-link to="/">Back</router-link>
    <div class="book-wrap">
      <div class="book-cover" :class="'book-id-' + book.id">
        <h1>{{ book.title }}</h1>
        <p>{{ book.author }}</p>
      </div>
      <div>
        <h1>{{ book.title }}</h1>
        <p>{{ book.author }}</p>
      </div>
    </div>

    <div></div>

    <!-- {{ $route.params.id }} -->
  </div>
</template>

<script>
export default {
  data: () => ({ bookID: "" }),
  computed: {
    book() {
      let books = this.$root.$data.books;
      let id = this.$route.params.id;
      let book = books.filter(b => b.id == id);
      return book[0];
    }
  }
};
</script>

<style lang="scss">
.book {
}

.book-wrap {
  display: flex;
  height: 300px;
}

.book-cover {
  margin: 0 20px;
}
</style>
