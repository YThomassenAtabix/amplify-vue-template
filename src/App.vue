<script setup lang="ts">
import Todos from './components/Todos.vue'
import { Authenticator } from "@aws-amplify/ui-vue";
import "@aws-amplify/ui-vue/styles.css";
</script>

<template>
  <main>
    <authenticator v-slot="{ signOut }">
        <Todos />
        <button @click="signOut">Sign out</button>
    </authenticator>
  </main>
</template>

