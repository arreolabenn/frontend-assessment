<template>
  <div>
    <base-banner
      :is-fancy="true"
      v-show="banner.image"
      :banner="banner">
    </base-banner>
  </div>
</template>

<script>
import BaseBanner from '~/components/base/BaseBanner.vue'

export default {
  components: {
    BaseBanner
  },

  props: {},

  data() {
    return {
      banner: {}
    }
  },

  beforeMount() {
    this.getBannerInfo()
  },

  methods: {
    getBannerInfo(){
      // Pretend GET request
      this.banner = {
        "title": "Hello Developer!",
        "content": "Lorem ipsum dolor sit amet, consectetur adipiscing elit",
        "image": "https://drive.google.com/uc?id=1_s7l2ICmBqE1v6oyennN9m-P9a_XdwsA",
        "image_mobile": "https://drive.google.com/uc?id=1Nm6EiyMzNAGq6lv9_4Io6MIE9gLwIMJC",
      }
    }
  },

  computed: {}
}
</script>

<style scoped>
</style>
