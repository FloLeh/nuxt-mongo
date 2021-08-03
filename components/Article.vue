<template>
  <div class="article">
    <h4>{{title}}</h4>
    <img :src="require(`~/assets/images/${photoUrl}.jpg`)">
    <div>
      <p>
        {{description}}
      </p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    'title': {
      type: String,
      default: ''
    }, 
    'photoUrl': {
      type: String,
      default: ''
    }, 
    'description': {
      type: String,
      default: ''
    }
  }
}
</script>

<style scoped>
  p {
    text-align: justify;
  }

  img {
    width: 100%;
  }

  .article {
    padding: 2px 20px;
    box-shadow: 2px 2px 8px rgba(0, 0, 0, 0.1);
    background-color: #ffffff;
  }
</style>