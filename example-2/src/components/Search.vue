<template>
  <form v-on:submit.prevent="handleText">
    <input type="text" v-on:keyup="handleText" v-model="text" />
    <button type="submit">Search</button>
  </form>
</template>

<script>
export default {
  props: {
    onText: Function,
  },
  data() {
    return {
      text: "",
    };
  },
  methods: {
    handleText() {
      this.onText(this.text);
    },
  },
};
</script>