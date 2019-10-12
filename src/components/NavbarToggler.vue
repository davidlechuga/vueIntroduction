<template>
  <button
    class="navbar-toggler"
    type="button"
    data-toggle="collapse"
    aria-expanded="false"
    :data-target="dataTarget"
    :aria-controls="ariaControls"
    :aria-label="ariaLabel"
  >
    <span class="navbar-toggler-icon" />
  </button>
</template>
<script>
const stringDefault = {
  type: String,
  default: ''
}
export default {
  name: 'NavbarToggler',
  props: {
    dataTarget: stringDefault,
    ariaControls: stringDefault,
    ariaLabel: stringDefault
  }
}
</script>
<style scoped>
</style>
