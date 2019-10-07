<template>
  <div>
    <form v-if="!connection_status" v-on:submit.prevent="onSubmit">
      <p v-if="errors.length">{{ this.errors }}</p>
      <p>
        <label for="username">Username:</label>
        <input type="text" name="username" id="username" v-model="username" autocomplete="username" />
      </p>
      <p>
        <label for="password">Password:</label>
        <input type="password" name="password" v-model="password" autocomplete="current-password" />
      </p>
      <input type="submit" value="Submit" />
    </form>
    <p v-if="connection_status">
      <apiVersion></apiVersion>
    </p>
  </div>
</template>

<script>
import { onLogin } from "@/vue-apollo";
import apiVersion from "@/components/Version.vue";

export default {
  name: "Login",
  components: {
    apiVersion
  },
  data: () => {
    return {
      username: null,
      password: null,
      errors: [],
      connection_status: null
    };
  },
  methods: {
    async onSubmit(e) {
      this.errors = [];

      if (!this.username) {
        this.errors.push("No username");
      }

      if (!this.password) {
        this.errors.push("No password");
      }

      this.connection_status = "Hello " + this.username;

      await onLogin(this.$apollo.provider.defaultClient, "coucou");
    }
  }
};
</script>