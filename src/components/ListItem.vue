<template>
  <span>{{x}},{{ gen }}</span>
</template>

<script>
/* eslint-disable */
export default {
  name: 'ListItem',
  props: {
    x: {
      type: String,
      required: true
    },
    i: {
      type: Number,
      required: true
    }
  },
  computed: {
    gen () {
      console.log('[ListItem] reactive call' + this.i)
      return `test${this.i}`
    }
  }
}
</script>