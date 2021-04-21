<template>
  <div>
    <div class="banner-container" :class="{'is-fancy': isFancy === true}">
      <div class="content-container">
        <img v-show="banner.image" :src="`${banner.image}`"
             class="image image-desktop is-hidden-mobile" >

        <img v-show="banner.image_mobile" :src="`${banner.image_mobile}`"
             class="image image-mobile is-hidden-tablet">

        <div class="image-tint" :class="{'is-fancy': isFancy === true}"></div>

        <div class="text-container">
          <h1 class="text-title" :class="{'is-fancy': isFancy === true}">
              {{ banner.title }}
          </h1>
          <h2 class="text-subtitle" :class="{'is-fancy': isFancy === true}">
            {{ banner.content }}
          </h2>    
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  layout: 'nonav',

  components: {},

  data() {
    return {}
  },

  props: {
    banner: {
      required: true,
    },

    isFancy: {
      required: false,
      default: false
    }
  },

  methods: {},

  computed: {}
}
</script>

<style>
  .banner-container {
    position: relative;
    background-repeat: no-repeat;
    background-size: cover;
    margin-bottom: 80px;
  }

  .banner-container .content-container {
    position: relative;
    width: 100%;
    height: 100%;
  }

  .banner-container .content-container .image {
    position: relative;
  }

  .banner-container .content-container .image.image-desktop {
    position: relative;
    object-fit: cover;
    width: 100vw;
    height: 60vh;
  }

  .banner-container .content-container .image.image-mobile {
    position: relative;
    object-fit: cover;
    width: 100vw;
    height: 100vh;
  }

  .banner-container .content-container .image-tint{
    position: absolute;
    transform: translate(50%, -50%);
    background-repeat: no-repeat;
    background: rgba(0, 0, 0, 0.25);
    background-size: cover;
    height: 100%;
    width: 100vw;
    right: 50%;
    top: 50%;
  }

  .banner-container .content-container .image-tint.is-fancy{
    background: linear-gradient(to right, rgba(0,0,0,0.25) 0%, rgba(0,0,0,0.75) 100%);
  }

  .banner-container .content-container .text-container {
    position: absolute;
    text-align: center;
    transform: translate(50%, -50%);
    width: 100vw;
    right: 50%;
    top: 50%;
  }

  .banner-container .content-container .text-container .text-title {
    font-size: 4.33rem !important;
    font-weight: 600;
    color: #FFF;
  }

  .banner-container .content-container .text-container .text-title.is-fancy {
    text-shadow: 2px 2px rgba(0,0,0,0.25);
  }

  .banner-container .content-container .text-container .text-subtitle {
    font-size: 2rem !important;
    font-weight: 400;
    color: #FFF;
  }

  .banner-container .content-container .text-container .text-subtitle.is-fancy {
    text-shadow: 1px 1px rgba(0,0,0,0.25);
  }
</style>
