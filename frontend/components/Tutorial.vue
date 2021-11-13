<template>
  <div>
    <ul>
      <li v-for="tweet in tweets" :key="tweet.id" v-text="tweet.body"></li>
    </ul>
  </div>
</template>

<script>
export default {
  data: () => ({
    tweets: []
  }),
  async fetch() {
    this.tweets = await this.$axios.$get('http://localhost:1337/tweets')
  },
}
</script>
