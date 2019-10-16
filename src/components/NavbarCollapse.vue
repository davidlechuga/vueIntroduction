<template>
  <div
    :id= "id"
    class="collapse navbar-collapse"
    :class="{show: active}"
  >
    <slot
    />

  </div>
</template>

<script>
export default {
  name: 'NavbarCollapse',
  props: {
    id: {
      type: [Number, String],
      default: ''
    },
    active: {
      type: Boolean,
      default: false
    }
  }
}

</script>

<style>

</style>
