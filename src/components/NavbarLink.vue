<template>
  <a
    class="nav-link"
  >
    {{ text }}
    <span class="sr-only">
      {{ label }}
    </span>
  </a>
</template>
<script>
const defaultString = {
  type: String,
  default: ''
}
export default {
  name: 'NavbarNavLink',
  props: {
    text: defaultString,
    label: defaultString
  }
}
</script>
<style scoped>
</style>
