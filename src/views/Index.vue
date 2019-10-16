<template>
  <div class="index">
    <post-card-list
      :posts="posts"
    />
  </div>
</template>

<script>
import PostCardList from '../components/PostCardList'
import api from '../lib/api'

export default {
  name: 'Index',
  components: {
    PostCardList
  },
  data () {
    return {
      posts: []
    }
  },
  async mounted () {
    const posts = await api.getPosts()

    this.posts = posts.map((post) => ({
      src: post.image,
      alt: post.title,
      title: post.title,
      text: post.description,
      butttonTo: `/post/${post._id}`,
      buttonText: 'ver detalle'
    }))
  }
}
</script>

<style scoped>
h1 {
  color: red;
}
</style>
