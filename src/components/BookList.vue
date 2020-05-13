<template>
  <div>
    <h1>
      {{ title }}
    </h1>
    <ul>
      <Book-Item v-for="book in books" :key="book.title">
        {{ book.title }}: {{ book.author }}
      </Book-Item>
    </ul>
  </div>
</template>

<script>
import BookItem from "./BookItem";
export default {
  components: { BookItem },
  name: "BookList",
  data() {
    return {
      title: "All Books",
      books: [
        { title: "Self-Reliance", author: "Ralph Waldo Emerson" },
        { title: "American Gods", author: "Neil Gaiman" },
        { title: "Amusing Ourselves to Death", author: "Neil Postman" },
      ],
    };
  },
};
</script>

<style>
h1,
h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: block;
  margin: 0 10px;
}
</style>
