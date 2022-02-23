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
$gradient-border-color: #35368f;
$gradient-hover-color: #8385fb52;

.list {
  &__item {
    position: relative;
    padding: 16px 32px 10px 32px;
    transition: all 0.3s ease-in-out;
    cursor: pointer;

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
        $gradient-border-color 30%,
        $gradient-border-color 50%,
        $gradient-border-color 70%,
        rgba(0, 0, 0, 0) 100%
      );
      opacity: 0.5;
    }

    &::before {
      position: absolute;
      bottom: 0;
      left: 0px;
      width: 100%;
      height: 100%;
      content: "";
      background: linear-gradient(
        90deg,
        rgba(0, 0, 0, 0) 0%,
        $gradient-hover-color 20%,
        $gradient-hover-color 50%,
        $gradient-hover-color 80%,
        rgba(0, 0, 0, 0) 100%
      );
      opacity: 0;
      transition: all 0.3s ease-in-out;
    }

    &:hover {
      &::before {
        opacity: 1;
      }

    }
  }
}
</style>