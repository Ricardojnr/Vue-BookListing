<template>
  <form v-on:submit.prevent="onSubmit" class="" action="#" method="post">
    <input
      v-model="bookTitle"
      type="text"
      name="title"
      value=""
      placeholder="Book Title"
    />
    <input
      v-model="bookAuthor"
      type="text"
      name="author"
      value=""
      placeholder="Book Author"
    />
    <button type="submit" name="button">Add Book</button>
  </form>
</template>
<script>
export default {
  name: "BookForm",
  props: ["books"],

  data() {
    return {
      bookTitle: "",
      bookAuhtor: "",
    };
  },
  methods: {
    bookSubmit(bookTitle, bookAuhtor) {
      this.$emit("addBook", bookTitle, bookAuhtor);
    },
  },
};
</script>
<style></style>
