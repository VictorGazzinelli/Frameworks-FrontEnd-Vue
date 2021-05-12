<template>
  <div id="app">
    <Search :onText="handleSearch" />
    <Form :onClick="handleAdd" />
    <List :items="listedItems.length > 0 ? listedItems : items" />
  </div>
</template>

<script>
import Search from "./components/Search.vue";
import Form from "./components/Form.vue";
import List from "./components/List.vue";

export default {
  name: 'App',
  components: {
    Form,
    List,
    Search,
  },
  methods: {
    handleSearch(text) {
      const results = this.items.filter((item) => item.name.includes(text));
      this.listedItems = results.length > 0 ? results : this.items;
    },
    handleAdd(item) {
      this.items = this.items.concat({
        id: this.items.length + 1,
        ...item,
      });
    },
  },
  data() {
    return {
      items: [],
      listedItems: [],
    };
  },
}
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
