<template>
  <router-link
    class='nav-link'
    :to="to"
  >
    {{ text }}
    <span
      class='sr-only'
    >
      {{ label }}
    </span>
  </router-link>
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
    label: defaultString,
    to: defaultString
  }
}

</script>
<style scoped>
</style>
