<template>
  <div class="content">
    <div class="card">
      <div class="card__item" v-for="(note, index) in guitarNotes" :key="index+note">
        {{ note }}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    guitarNotes: {
      type: Array,
    }
  }
};
</script>

<style lang="scss" scoped>
.content {
  display: flex;
  justify-content: center;
  align-items: center;
  background: #e5e9fd;

  .card {
    display: flex;
    background: #f4f6f7;
    padding: 10px;
    border-radius: 6px;

    &__item {
      margin-right: 10px;
      background: #8384fb;
      padding: 20px;
      color: white;
      border-radius: 6px;
      font-size: 36px;
    
      &:last-child {
        margin-right: 0px;
      }
    }
  }
}
</style>