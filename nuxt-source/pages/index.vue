<template>
  <section class="section">
    <div class="container">
    </div>
  </section>
</template>

<script>
export default {
  layout: 'nonav',

  components: {},

  data() {
    return {}
  },

  beforeMount() {
    this.$nuxt.$router.replace({ path: `/assessments/one` })
  },

  methods: {},

  computed: {}
}
</script>

<style scoped>
</style>
