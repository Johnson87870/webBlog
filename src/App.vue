<template>
  <div id="app">
    <Menus />
    <div class="container">
      <router-view />
    </div>
  </div>
</template>

<script>
import menus from "@/components/Menus";
export default {
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
  display: flex;
  > .container {
    padding-left: 20px;
  }
}
</style>
