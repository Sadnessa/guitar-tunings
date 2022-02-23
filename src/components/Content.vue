<template>
  <div class="content">
    <div class="card">
      <div class="card__item" v-for="note in guitarNotes" :key="note">
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
  background: #d7dbf0;

  .card {
    display: flex;
    background: white;
    padding: 10px;
    border-radius: 6px;

    &__item {
      margin-right: 10px;
      background: gray;
      padding: 20px;
    
      &:last-child {
        margin-right: 0px;
      }
    }
  }
}
</style>