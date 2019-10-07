<template>
  <div>{{ingredient}}</div>
</template>

<script>
import gql from "graphql-tag";
import API_VERSION from "../graphql/Version.gql";
import INGREDIENT from "../graphql/Ingredient.gql";

export default {
  name: "Recipeql",
  apollo: {
    apiVersion: API_VERSION,
    ingredient: {
      query: INGREDIENT
      //pollInterval: 300
    }
  }
};
</script>