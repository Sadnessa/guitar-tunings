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
    background: white;
  }
}
</style>