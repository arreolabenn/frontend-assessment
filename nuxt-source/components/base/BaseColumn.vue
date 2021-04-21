<template>
  <div class="columns">
    <div class="column" :class="`${columnSize} ${columnOffset}`">
      <slot name="child-component"></slot>
    </div>
  </div>
</template>

<script>
export default {
  components: {},

  props: {
    columnSize: {
      type: String,
      required: false,
      default: 'is-10'
    },

    columnOffset: {
      type: String,
      required: false,
      default: 'is-offset-1'
    },
  },

  data() {
    return {}
  },

  methods: {},

  computed: {}
}
</script>

<style scoped>
</style>
