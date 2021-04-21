<template>
  <div v-if="contentData" class="columns">
    <div v-for="item, index in contentData" class="card column is-4 custom-card">
      <div class="card-image custom-card-image">
        <figure class="image is-4by3">
          <img src="http://via.placeholder.com/400x300">
        </figure>
      </div>
      <div class="card-content">
        <p class="custom-content has-text-centered">
          {{ item.content }}
        </p>

        <button class="custom-button">
            <b>READ MORE</b>
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  components: {},

  props: {},

  data() {
    return {
      contentData: []
    }
  },

  beforeMount() {
    this.getContentInfo()
  },

  methods: {
    getContentInfo(){
      // Pretend GET request
      this.contentData = [
        {
          "title": "Section 1",
          "content": "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer mattis, nisl ut eleifend suscipit, orci ex lobortis metus, quis dictum felis augue eu ex. Curabitur felis felis, tempor eu ante id, blandit pulvinar eros. Aliquam pretium, sem in pulvinar convallis, ipsum enim facilisis diam, vel dapibus orci nunc eu enim."
        },
        {
          "title": "Section 2",
          "content": "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer mattis, nisl ut eleifend suscipit, orci ex lobortis metus, quis dictum felis augue eu ex."
        },
        {
          "title": "Section 3",
          "content": "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer mattis, nisl ut eleifend suscipit, orci ex lobortis metus, quis dictum felis augue eu ex. Curabitur felis felis, tempor eu ante id, blandit pulvinar eros."
        }
      ]
    }
  },

  computed: {}
}
</script>

<style scoped>
  .card-content .custom-content {
    margin-bottom: 60px;
   }

 .card-content .custom-button {
  position: absolute;
  height: 40px;
  width: 200px;
  border-style: solid;
  border-width: 3px;
  border-color: #333;
  border-radius: 50px;
  background: white;
  font-weight: 600;
  color: #000;
  bottom: 30px;
  right: 50%;
  font-size: 15px;
  transform: translate(50%, 0);
  letter-spacing: 2px;
 }

 .card.is-4 {
  margin: 1% !important;
  width: 30% !important;
 }

 .card.custom-card {
    border-radius: 20px;
 }

  .card-image.custom-card-image {
    border-radius: 10px;
    padding: 10px;
  }

  .card-image.custom-card-image .image img{
    border-radius: 10px;
  }

  @media screen and (max-width: 768px) {
    .card.is-4 {
      margin: 6% !important;
      margin-bottom: 10% !important;
      width: 88% !important;
     }
  }

</style>


