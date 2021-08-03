<template>
  <div>
    <h2>Les articles actuellement à vendre :</h2>
    <div class='articles'>
      <div v-for="article in articles" :key="article.title">
        <Article :title="article.title" :description="article.description" :photo-url="article.imageUrl"/>
      </div>
    </div>
  </div>
</template>

<script>
import articles from '../articles.json'

export default {
  data() {
    return {articles}
  }
}
</script>

<style scoped>
  .articles {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 40px;
  }
</style>