<template>
<div class="container">
  <form @submit.prevent="onsubmit">
    <form-input
      id="email"
      name="email"
      type="email"
      placeholder="lechugazteca@hotmail.com"
      aria-described-by="email for login"
      label="Email"
      @change="onChangeValue"
      @input="onChangeValue"
      required
    />
    <form-input
      id="password"
      name="password"
      type="password"
      placeholder="*****"
      aria-described-by="password for login"
      label="Password"
      @change="onChangeValue"
      @input="onChangeValue"
      required
    />
    <form-input
      id="description"
      name="description"
      placeholder="Este es un post bien perron"
      aria-described-by="post description"
      label="Descripción"
      @change="onChangeValue"
      @input="onChangeValue"
      required
    />

     <button
      class="btn btn-primary"
      type="submit"
    >
      Login
    </button>
  </form>
</div>

</template>

<script>

import FormInput from '../components/FormInput'
import api from '../lib/api'

export default {
  name: 'Login',
  components: {
    FormInput
  },
  data () {
    return {
      email: '',
      password: '',
      loading: false
    }
  },
  methods: {
    onChangeValue (event) {
      const { name, value } = event.target
      this[name] = value
    },
    async onsubmit () {
      this.loading = true

      const { token } = await api.login(this.email, this.password)
      sessionStorage.setItem('Token', token)

      this.loading = false
      this.$router.push('/new-post')
    }
  },
  beforeRouteEnter (to, from, next) {
    const token = sessionStorage.getItem('token')

    if (!token) next()
    else next('/login')
  }
}

</script>

<style scoped>

</style>
