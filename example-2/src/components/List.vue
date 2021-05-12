<template>
  <div>
    <ul>
      <li v-for="item in items" :key="item.id">
        <ListItem :item="item" />
      </li>
    </ul>
    {{ totalItems }}
  </div>
</template>

<script>
import ListItem from "./ListItem.vue";

export default {
  props: {
    items: Array,
  },
  components: {
    ListItem,
  },
  computed: {
    totalItems() {
      const total = this.items.length;
      return total > 1 ? `Total: ${total} items` : `Total: ${total} item`;
    },
  },
};
</script>
