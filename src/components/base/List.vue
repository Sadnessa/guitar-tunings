<template>
  <div class="list">
    <div class="list__item" v-for="item in items" :key="item" @click="$emit('update:modelValue', item)">
      {{ item }}
    </div>
  </div>
</template>

<script>
export default {
  props: {
    items: {
      type: Array,
    },
  },
};
</script>

<style lang="scss" scoped>
$gradient-border-color: rgb(122, 122, 122);
// $gradient-hover-color: rgba(255, 255, 255, 0.514);

.list {
  &__item {
    position: relative;
    padding: 16px 32px 10px 32px;
    transition: all 0.3s ease-in-out;

    &::after {
      position: absolute;
      bottom: 0px;
      content: "";
      width: 95%;
      height: 2px;
      left: 50%;
      transform: translateX(-50%);
      background: linear-gradient(
        90deg,
        rgba(0, 0, 0, 0) 0%,
        $gradient-border-color 20%,
        $gradient-border-color 50%,
        $gradient-border-color 80%,
        rgba(0, 0, 0, 0) 100%
      );
    }

    &:hover {
      // background: linear-gradient(180deg, rgba(0,0,0,0) 0%, $gradient-hover-color 20%,  $gradient-hover-color 70%, rgba(0,0,0,0) 100%);
      background: rgba(255, 255, 255, 0.438);

      &::after {
        height: 0px;
      }
    }
  }
}
</style>