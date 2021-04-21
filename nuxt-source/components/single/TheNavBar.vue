<template>
  <b-navbar :class="{'is-primary': $nuxt.$route.path === '/assessments/two'}">
    <template #start>
      <b-navbar-item 
        v-for="item, index in navItems" :key="`nav_item_${index}`"
        class="navbar-item navbar-item-padding" :href="`${item.link}`">
        <span :class="{'has-text-weight-bold': $nuxt.$route.path === item.link}">
          {{ item.label }}
        </span>
      </b-navbar-item>
    </template>
  </b-navbar>
</template>

<script>
export default {
  components: {},

  props: {},

  data() {
    return {
      navItems: [
        {
          label: 'Assessment 1',
          link: '/assessments/one'
        },
        {
          label: 'Assessment 2',
          link: '/assessments/two'
        }
      ]
    }
  },

  methods: {},

  computed: {}
}
</script>

<style scoped>
  .navbar-item-padding {
    padding-left: 20px;
    padding-right: 20px;
  }
</style>
