<template>
  <div>
    <the-nav-bar></the-nav-bar>
    <nuxt></nuxt>
    <span class="add-signature"> by /arreolabenn</span>
  </div>
</template>

<script>
import TheNavBar from '~/components/single/TheNavBar.vue'

export default {
  components: {
    TheNavBar
  },

  props: {},

  data() {
    return {}
  },

  beforeMount() {},

  methods: {},

  computed: {}
}
</script>

<style scoped>
  .add-signature {
    display: block;
    text-align: right;
    margin-top: 100px;
    margin-bottom: 15px;
    padding-right: 20px;
  }
</style>
