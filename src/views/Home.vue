<template>
  <div class="home">
    <h1>8 Classic Childrens books</h1>
    <div class="books">
      <!-- <router-link to="/">Home</router-link> |
      <router-link to="/book">Book</router-link> -->
      <router-link
        v-bind:to="'/book/' + book.id"
        v-for="book in books"
        v-bind:key="book.id"
      >
        <div class="book">
          <p class="title">{{ book.title }}</p>
          <p class="author">{{ book.author }}</p>
        </div>
      </router-link>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from "@/components/HelloWorld.vue";
// import book from "./Book.vue";

export default {
  name: "Home",
  computed: {
    books() {
      return this.$root.$data.books;
    }
  }
};
</script>
