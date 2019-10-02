<template>
  <div class="home">
    <Recipeql></Recipeql>
  </div>
</template>

<script>
// @ is an alias to /src
import Recipeql from "@/components/Recipeql.vue";

export default {
  name: "home",
  components: {
    Recipeql
  }
};
</script>
