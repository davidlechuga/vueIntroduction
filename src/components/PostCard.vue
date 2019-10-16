<template>
 <div class="card">
    <img
      :src="src"
        class="card-img-top"
      :alt="alt"
    >

    <div class="card-body">
      <h5
        class="card-title"
        >
        {{title}}
      </h5>
      <p
        class="card-text"
        >
        {{text}}
      </p>
      <RouterLink
        :to="buttonTo"
        class="btn btn-primary"
      >
        {{buttonText}}
      </RouterLink>
    </div>
  </div>
</template>

<script>
const stringDefault = {
  type: String,
  required: true
}

export default {
  name: 'PostCard',
  props: {
    src: stringDefault,
    alt: stringDefault,
    title: stringDefault,
    text: stringDefault,
    buttonTo: stringDefault,
    buttonText: stringDefault
  }
}
</script>

<style scoped>

</style>
