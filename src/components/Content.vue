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
  padding: 30px;
  box-sizing: border-box;
  background: #e5e9fd;
  font-family: 'Mochiy Pop One', sans-serif;

  .card {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    background: #f4f6f7;
    padding: 10px;
    border-radius: 6px;
    box-shadow: rgba(99, 99, 99, 0.2) 0px 2px 8px 0px;

    &__item {
      min-width: 50px;
      margin: 10px;
      background: #8384fb;
      padding: 20px;
      color: white;
      border-radius: 6px;
      font-size: 36px;
      text-align: center;
    }
  }
}
</style>