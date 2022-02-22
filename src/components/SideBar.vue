<template>
  <div class="sidebar">
    <List :items="items"></List>
    </div>
</template>

<script>
import List from "./base/List.vue";

export default {
  components: {
    List,
  },

  props: {
    items: {
      type: Array,
    }
  }
};
</script>

<style lang="scss" scoped>
.sidebar {
  background: #afb0cf;
}
</style>