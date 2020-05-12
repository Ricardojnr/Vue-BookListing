<template>
  <li>{{ book.title }} : {{ book.author }}</li>
</template>
<script>
export default {
  name: "BookItem",

  data() {
    props["book"];
    return {
      key: value,
    };
  },
};
</script>

<style>
li {
  display: block;
  margin: 0 10px;
}
</style>
