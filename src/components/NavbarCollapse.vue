<template>
  <div
    :id= "id"
    class="collapse navbar-collapse"
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
    }
  }
}

</script>

<style>

</style>
