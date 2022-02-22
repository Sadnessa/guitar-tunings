<template>
  <Header></Header>
  <div class="main">
    <SideBar :items="listItems"></SideBar>
    <Content></Content>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import SideBar from "./components/SideBar.vue";
import Content from "./components/Content.vue"

export default {
  components: {
    Header,
    SideBar,
    Content,
  },

  data() {
    return {
      listItems: ['fdfsds', 'fdssdfsdf']
    }
  }
};
</script>

<style lang="scss">
#app {
  display: flex;
  flex-direction: column;
  height: 100vh;
}

body {
  margin: 0px;
}
</style>

<style lang="scss" scoped>
.main {
  display: flex;
  flex: 1;

  .content {
    flex: 1;
    height: 100%;
    min-width: 50%;
  }

  .sidebar {
    width: 400px;
  }
}
</style>