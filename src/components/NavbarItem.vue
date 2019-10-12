<template>
  <li
  class="nav-item"
  :class="{ active, dropdown}"
  >
    <slot

    />

  </li>

</template>

<script>

const booleanDefault = {
  type: Boolean,
  default: false
}

export default {
  name: 'NavbarItem',
  props: {
    active: booleanDefault,
    dropdown: booleanDefault
  }
}
</script>

<style>

</style>
