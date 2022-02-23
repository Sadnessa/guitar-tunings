<template>
  <Header></Header>
  <div class="main">
    <SideBar :items="listItems" v-model="activeListItem"></SideBar>
    <Content :guitarNotes="itemNotes"></Content>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import SideBar from "./components/SideBar.vue";
import Content from "./components/Content.vue";

export default {
  components: {
    Header,
    SideBar,
    Content,
  },

  data() {
    return {
      guitarRank: [
        { name: "Standard", notes: ["E", "A", "D", "G", "B", "E"] },
        { name: "Dropped D", notes: ["D", "A", "D", "G", "B", "E"] },
        { name: "Dropped C", notes: ["C", "G", "C", "F", "A", "D"] },
      ],
      activeListItem: "Standard",
    };
  },

  computed: {
    listItems() {
      let arrName = [];
      for (var i = 0; i < this.guitarRank.length; i++) {
        arrName.push(this.guitarRank[i].name);
      }
      return arrName;
    },

    itemNotes() {
      for (var i = 0; i < this.guitarRank.length; i++) {
        if (this.activeListItem == this.guitarRank[i].name) {
          return this.guitarRank[i].notes;
        }
      }
    },
  },
};
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Mochiy+Pop+One&family=Permanent+Marker&family=Varela+Round&display=swap');

#app {
  display: flex;
  flex-direction: column;
  height: 100vh;
  font-family: 'Varela Round', sans-serif;
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