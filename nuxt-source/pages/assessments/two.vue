<template>
  <div>
    <the-banner/>
    <base-column v-slot:child-component="child">
      <the-content :itinerary="child.item"></the-content>
    </base-column>
  </div>
</template>

<script>
import TheBanner from '~/components/pages/assessment/two/TheBanner.vue'
import TheContent from '~/components/pages/assessment/two/TheContent.vue'

import BaseColumn from '~/components/base/BaseColumn.vue'

export default {
  layout: 'default',

  components: {
    TheBanner,
    TheContent,
    BaseColumn
  },

  data() {
    return {}
  },

  beforeMount() {},

  methods: {},

  computed: {}
}
</script>

<style scoped>
</style>
