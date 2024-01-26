<script setup lang="ts">
import { Authenticator } from "@aws-amplify/ui-vue";
import { Amplify } from "aws-amplify";
import config from "../amplifyconfiguration.json";
Amplify.configure(config);
import "@aws-amplify/ui-vue/styles.css";
</script>

<template>
  <header></header>

  <main>
    <h1>Hello World</h1>
    <Authenticator>
      <template #="{ signOut }">
        <div class="center">
          <h1>Welcome signed in</h1>
          <button @click="signOut">Sign Out</button>
        </div>
      </template>
    </Authenticator>
  </main>
</template>

<style scoped></style>
