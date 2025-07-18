<template>
  <div>
    <h2>Login</h2>
    <input v-model="user" placeholder="Usuario" />
    <input v-model="pass" type="password" placeholder="Clave" />
    <button @click="login">Entrar</button>
  </div>
</template>

<script>
export default {
  data() {
    return { user: '', pass: '' }
  },
  methods: {
    login() {
      if (this.user === 'admin' && this.pass === 'clave123') {
        this.$router.push('/admin')
      } else {
        alert('Usuario o clave incorrectos')
      }
    }
  }
}
</script>