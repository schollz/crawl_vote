<template lang="pug">
form(v-on:submit.prevent="joinCrawl")
  .pb-4
    label.block.pb-1.font-medium.text-sm.text-blue-light.uppercase.tracking-wide(for="token") Code
    input.shadow.appearance-none.border.rounded.w-full.py-2.px-3(type="text" id="token" v-model="token")
  .pt-2
    input.btn.btn--active.w-full(type="submit" value="Join Crawl")
</template>

<script>
export default {
  data: function() {
    return {
      token: ''
    }
  },

  methods: {
    joinCrawl: function() {
      window.location.href = '/crawls/' + this.token.toLowerCase()
    }
  }
}
</script>
