<template>
  <div class="sidebar">
    <List :items="items" @update:modelValue="$emit('update:modelValue', $event)"></List>
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
    },

    modelValue: {
      type: String,
    }
  }
};
</script>

<style lang="scss" scoped>
.sidebar {
  background: #f4f6f7;
}
</style>