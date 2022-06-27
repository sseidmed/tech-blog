<template>
  <Layout>
    <div class="markdown-body">
      <h1>{{ $page.post.title }}</h1>
      <PostMeta :post="$page.post" />
      <br>
      <div v-html="$page.post.content" />
    </div>
  </Layout>
</template>

<page-query>
query Post ($path: String!) {
  post: post (path: $path) {
    title
    content
    date
  }
}
</page-query>

<script>
import PostMeta from '../components/PostMeta.vue'
export default {
  components: {
      PostMeta
  },
  metaInfo() {
    return {
      title: this.$page.post.title,
      date: new Date(this.$page.post.date).toDateString()
    }
  }
}
</script>

<style>

@import url('https://cdnjs.cloudflare.com/ajax/libs/github-markdown-css/5.1.0/github-markdown-light.min.css');

.markdown-body {
    box-sizing: border-box;
    min-width: 200px;
    max-width: 980px;
    margin: 0 auto;
    padding: 45px;
}

@media (max-width: 767px) {
    .markdown-body {
        padding: 15px;
    }
}

</style>