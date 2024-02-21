<script setup lang="ts">
const auth = useCookie('pokemon-auth')

const authenticate = () => {
  auth.value = '1r3g'
}

const logout = () => {
  auth.value = ''
}

</script>

<template>
  <div>
    <h1>Login</h1>

    <button @click="authenticate">Login</button>
    <button @click="logout">Logout</button>
  </div>
</template>

<style scoped>

</style>