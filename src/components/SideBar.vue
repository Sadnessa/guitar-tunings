<template>
  <div class="sidebar">
    <List :items="items" :modelValue="modelValue" @update:modelValue="$emit('update:modelValue', $event)"></List>
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
  box-shadow: rgba(99, 99, 99, 0.2) 0px 2px 8px 0px;
  z-index: 1;
}
</style>