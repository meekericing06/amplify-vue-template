<script setup lang="ts">
import Todos from './components/Todos.vue'

import { Authenticator } from "@aws-amplify/ui-vue";
import "@aws-amplify/ui-vue/styles.css";

</script>

<template>
  <main>
    
    <authenticator>
      <template v-slot="{ signOut }">
        <h1>Hello Blah {{user?.signInDetails?.loginId}}'s todos</h1>
        <Todos />
        <button @click="signOut">Sign Out</button>
      </template>
    </authenticator>
      </main>
</template>

