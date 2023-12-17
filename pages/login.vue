<script setup lang="ts">
const userEmail = ref('')
const userPassword = ref('')

const userLogin = ref(false)

const handleLogin = () => {
  if (userPassword.value === '123')
    userLogin.value = true
}

</script>

<template>
  <h2>strona statyczna</h2>
  <h1>Strona logowania</h1>
  <div class="field">
    <p class="control has-icons-left has-icons-right">
      <input class="input" type="email" placeholder="Email" v-model="userEmail">
      <span class="icon is-small is-left">
      <i class="fas fa-envelope"></i>
    </span>
      <span class="icon is-small is-right">
      <i class="fas fa-check"></i>
    </span>
    </p>
  </div>
  <div class="field">
    <p class="control has-icons-left">
      <input class="input" type="password" placeholder="Password" v-model="userPassword">
      <span class="icon is-small is-left">
      <i class="fas fa-lock"></i>
    </span>
    </p>
  </div>
  <div class="field">
    <p class="control">
      <button class="button is-success" type="button" @click="handleLogin">
        Login
      </button>
    </p>
  </div>
  <User v-if="userLogin">
    {{ userEmail }}
  </User>
</template>

<style scoped>

</style>