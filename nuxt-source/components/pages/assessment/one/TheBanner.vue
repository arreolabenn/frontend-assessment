<template>
  <div>
    <base-banner
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
        "image": "http://via.placeholder.com/1920x650.png",
        "image_mobile": "http://via.placeholder.com/600x600",
      }
    }
  },

  computed: {}
}
</script>

<style scoped>
</style>
