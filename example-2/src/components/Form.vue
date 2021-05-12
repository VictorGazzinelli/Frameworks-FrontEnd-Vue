<template>
  <form v-on:submit.prevent="addItem">
    <input type="text" v-model="name">
    <button type="submit">Register</button>
  </form>
</template>

<script>
export default {
  props: {
    onClick: Function
  },
  data() {
    return {
      name: ""
    };
  },
  methods: {
    addItem() {
      const item = {
        name: this.name
      };

      this.onClick(item);
      this.name = '';
    }
  }
};
</script>
