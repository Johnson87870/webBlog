<template>
  <div id="app">
    <Menus v-show="!(path === '/welcome')" />
    <div class="container">
      <router-view />
    </div>
  </div>
</template>

<script>
import menus from "@/components/Menus";
export default {
  data() {
    return {
      path: ""
    };
  },
  mounted() {
    this.path = this.$route.path;
  },
  watch: {
    $route(to, from) {
      this.path = to.path;
    }
  },
  components: {
    Menus: menus
  }
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  background-color: #f5f5f5;
  display: flex;
  height: 100%;
  > .container {
    margin-top: 10px;
    margin-bottom: 10px;
    margin-left: 20px;
    margin-right: 20px;
    width: 80%;
    min-height: 100%;
    background-color: #fff;
  }
}
</style>
