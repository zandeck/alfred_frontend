<template>
  <div class="home">
    <Recipeql></Recipeql>
    <apiVersion></apiVersion>
    <Login></Login>
  </div>
</template>

<script>
// @ is an alias to /src
import Recipeql from "@/components/Recipeql.vue";
import apiVersion from "@/components/Version.vue";
import Login from "@/components/Login.vue";

export default {
  name: "home",
  components: {
    Recipeql,
    apiVersion,
    Login
  }
};
</script>
