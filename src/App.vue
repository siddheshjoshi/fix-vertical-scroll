<template>
  <div id="app">
    <button
      class="btn btn-primary"
      @click="openModal()"
    >click me</button>
  </div>
</template>

<script>
import MyModalVue from "./components/MyModal.vue";
export default {
  name: "App",
  components: {},
  methods: {
    openModal() {
      this.$modal.show(
        MyModalVue,
        {},
        {
          adaptive: true,
          height: "85%",
          width: "85%",
        },
        {
          closed: () => {
            console.log("closed");
          },
        }
      );
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
