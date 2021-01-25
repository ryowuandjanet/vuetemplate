<template>
  <p>Reaction time - {{ score }}</p>
  <p class="rank">{{ rank }}</p>
</template>

<script>
export default {
  props: ['score'],
  data() {
    return{
      rank: null
    }
  },
  mounted() {
    if (this.score < 500 ) {
      this.rank = '忍者等級'
    } else if (this.score < 800 ) {
      this.rank = '常人等級'
    } else {
      this.rank = '手殘等級'
    }
  }
}
</script>

<style scoped>
  .rank {
    font-size: 1.4em;
    color: #0faf87;
    font-weight: bold;
  }
</style>
