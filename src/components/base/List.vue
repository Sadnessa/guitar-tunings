<template>
  <div class="list">
    <div class="list__item" v-for="item in items" :key="item">
      {{ item }}
    </div>
  </div>
</template>

<script>
export default {
  props: {
    items: {
      type: Array,
    }
  }
}
</script>

<style lang="scss" scoped>

</style>