<template>
  <form @submit.prevent="OnSubmit">
    <form-input
      id="title"
      name="title"
      placeholder="El super post de la muerte"
      aria-described-by="title for the post"
      label="Titulo"
      @change="onChangeValue"
      @input="onChangeValue"
      required
    />

    <form-input
      id="readTime"
      type="number"
      name="readTime"
      placeholder="666min"
      aria-described-by="read time"
      label="Tiempo de lectura"
      @change="onChangeValue"
      @input="onChangeValue"
      required
    />

    <form-input
      id="description"
      name="description"
      placeholder="Este es un post bien perron"
      aria-described-by="post description"
      label="Descripción"
      @change="onChangeValue"
      @input="onChangeValue"
      required
    />
    <FormInput
      id="image"
      name="image"
      placeholder="https://inserte-meme-aqui.com"
      aria-described-by="image input"
      label="Imagén"
      @change="onChangeValue"
      @input="onChangeValue"
      required
    />

    <img
      v-if="image"
      :src="image"
      class="card-img-to"
      alt="meme-preview"
    >

    <button
      class="btn btn-primary"
      type="submit"
    >
      Save post
    </button>

  </form>
</template>

<script>
import FormInput from './FormInput'

export default {
  name: 'FormNewPost',
  components: {
    FormInput
  },
  data () {
    return {
      title: '',
      readTime: '',
      description: '',
      image: ''
    }
  },
  methods: {
    onChangeValue (event) {
      const { name, value } = event.target
      this[name] = value
    },
    OnSubmit () {
      this.$emit('submit', {
        title: this.title,
        readTime: this.readTime,
        description: this.description,
        image: this.image
      })
    }
  }
}
</script>

<style scoped>
  .btn.btn-primary {
    position: fixed;
    right: 2rem;
    bottom: 2rem;
  }
</style>
