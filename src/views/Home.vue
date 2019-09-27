<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <Recipeql></Recipeql>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";
import Recipeql from "@/components/Recipeql.vue";

export default {
  name: "home",
  components: {
    Recipeql
  }
};
</script>
