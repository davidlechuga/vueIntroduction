<template>
<div class="post-card-list container">
  <div
    class="row"
    v-for="(post, index) in posts"
    :key="index"
  >
    <post-card
      v-bind="post"
    />
  </div>
</div>
</template>

<script>
import PostCard from './PostCard'

export default {
  name: 'PostCardList',
  props: {
    posts: {
      type: Array,
      default: () => ([])
    }
  },
  components: {
    PostCard
  }
}
</script>

<style scoped>

</style>
