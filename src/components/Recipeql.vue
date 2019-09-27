<template>
  <div>{{apiVersion}}</div>
</template>

<script>
import gql from "graphql-tag";

export default {
  name: "Recipeql",
  apollo: {
    apiVersion: gql`
      query {
        apiVersion
      }
    `
  }
};
</script>