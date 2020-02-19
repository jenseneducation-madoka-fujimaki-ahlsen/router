<template>
  <div id="app">
    <div id="nav">
      <!-- <router-link to="/">Home</router-link> |
      <router-link to="/book">Book</router-link> -->
    </div>
    <router-view />
  </div>
</template>

<style lang="scss">
$bok-color-1: yellow;
$bok-color-2: blue;
$bok-color-3: green;
$bok-color-4: red;
$bok-color-5: purple;
$bok-color-6: white;
$bok-color-7: pink;
$bok-color-8: orange;

.books {
  display: grid;
  grid-template-columns: repeat(4, auto);
  grid-row: repeat(2, auto);
  grid-gap: 4px;
}
.book {
  height: 200px;
  border-left: 2px solid black;
}

.books a:nth-child(1),
.book-id-1 {
  background-color: $bok-color-1;
}
.books a:nth-child(2),
.book-id-2 {
  background-color: $bok-color-2;
}
.books a:nth-child(3),
.book-id-3 {
  background-color: $bok-color-3;
}
.books a:nth-child(4),
.book-id-4 {
  background-color: $bok-color-4;
}
.books a:nth-child(5),
.book-id-5 {
  background-color: $bok-color-5;
}
.books a:nth-child(6),
.book-id-6 {
  background-color: $bok-color-6;
}
.books a:nth-child(7),
.book-id-7 {
  background-color: $bok-color-7;
}
.books a:nth-child(8),
.book-id-8 {
  background-color: $bok-color-8;
}
.title {
  font-weight: 800;
}
</style>
