<template>
<span class="navbar-brand mb-0 h1">
    {{text}}
</span>

</template>

<script>
export default {
  name: 'NavbarBrand',
  props: {
    text: {
      type: String,
      default: ''
    }
  }
}
</script>

<style scoped>

</style>
