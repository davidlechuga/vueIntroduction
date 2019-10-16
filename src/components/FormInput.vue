<template>
  <div class="form-group">
      <label
        :for="id"
      >
        {{label}}
      </label>
      <input
        :name="name"
        :type="type"
        :id="id"
        :aria-describedby="arialDescribedBy"
        :placeholder="placeholder"
        :required="required"
        class="form-control"
        v-model="value"
        @input="$emit('input' , $event)"
        @change="$emit('change' , $event)"

      >
      <small
        v-if="help"
          :id="`${id}-help`"
          class="form-text text-muted"
      >
        {{help}}
      </small>
    </div>
</template>

<script>

const stringDefaul = {
  type: String,
  default: ''
}

export default {
  name: 'FormInput',
  props: {
    id: {
      type: [Number, String],
      required: true
    },

    label: stringDefaul,
    type: stringDefaul,
    arialDescribedBy: stringDefaul,
    placeholder: stringDefaul,
    help: stringDefaul,
    name: stringDefaul,
    required: {
      type: Boolean,
      default: false
    }

  },
  data () {
    return {
      value: null
    }
  }

}
</script>

<style scoped>

</style>
