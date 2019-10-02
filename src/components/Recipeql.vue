<template>
  <div>{{apiVersion}}</div>
</template>

<script>
import gql from "graphql-tag";
import API_VERSION from "../graphql/Version.gql";

export default {
  name: "Recipeql",
  apollo: {
    apiVersion: API_VERSION
  }
};
</script>