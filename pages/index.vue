<script setup lang="ts">
const { data: pokemon, error } = await useFetch('/api/popk')
</script>

<template>
  <div>
    <h1>Home page for Nuxt 3 server course</h1>

    <ul v-if="pokemon">
      <li>
        <img :src="pokemon?.sprite" alt="pokemon image" />
      </li>
      <li>{{ pokemon?.id }} {{ pokemon?.name }}</li>
    </ul>

    <div v-else>
      <p>{{ error }}</p>
    </div>
  </div>
</template>

<style scoped></style>
