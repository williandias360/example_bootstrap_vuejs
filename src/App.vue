<template>
  <div>
    <Toolbar />
    <div class="text-center">
      <h1>Example cards</h1>
    </div>
    <Cards />
  </div>
</template>

<script>
import Toolbar from "./components/Toolbar";
import Cards from "./components/Cards";
export default {
  name: "app",
  components: {
    Toolbar,
    Cards
  }
};
</script>

<style>
</style>
