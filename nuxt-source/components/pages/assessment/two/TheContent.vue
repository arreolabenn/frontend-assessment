<template>
  <div v-if="contentData" class="columns">
    <div class="is-hidden-mobile column is-12">
      <b-tabs v-model="isOpen" type="is-toggle" expanded>
          <b-tab-item v-for="item, index in contentData" :label="item.title">
            <span class="content" v-html="item.content"></span>
          </b-tab-item>
      </b-tabs>
    </div>

    <div class="is-hidden-tablet column is-12">
      <b-collapse
        class="card"
        animation="slide"
        v-for="(item, index) in contentData"
        :open="isOpen == index"
        @open="isOpen = index">
          <template #trigger="props">
            <div class="card-header" role="button">
              <p class="card-header-title">
                {{ item.title }}
              </p>
              <a class="card-header-icon">
                  <b-icon :icon="props.open ? 'menu-down' : 'menu-up'"></b-icon>
              </a>
            </div>
          </template>

          <div class="card-content">
              <div class="content">
                  <span v-html="item.content"></span>
              </div>
          </div>
        </b-collapse>
    </div>

  </div>
</template>

<script>
import content from '~/../data.json'

export default {
  components: {},

  props: {},

  data() {
    return {
      content,
      contentData: [],
      isOpen: 0
    }
  },

  beforeMount() {
    this.getContentInfo()
  },

  methods: {
    getContentInfo(){
      // Pretend GET request
      this.contentData = content
    }
  },

  computed: {}
}
</script>

<style scoped>
  @media screen and (max-width: 768px) {
    .column.is-12 {
      margin: 6% !important;
      margin-bottom: 10% !important;
      width: 88% !important;
     }
  }
</style>
