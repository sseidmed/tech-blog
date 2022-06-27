<template>
  <Layout>

    <!-- Learn how to use images here: https://gridsome.org/docs/images -->

    <ul>
      <li v-for="post in $page.posts.edges" :key="post.id">
        <g-link :to="post.node.path"> {{ post.node.title}} - {{ post.node.date }}
          </g-link>
      </li>
    </ul>
    <Pager :info="$page.posts.pageInfo" class="pager-container"
       linkClass="pager-container__link" showLinks/>

  </Layout>
</template>

<page-query>

query Posts ($page: Int) {
  posts: allPost (perPage: 5, page: $page) @paginate {
    pageInfo {
      totalPages
      currentPage	
      isFirst
      isLast
    }
    edges {
      node {
        id
        title 
        path
        date
      }
    }
  }
}

</page-query>


<script>
import { Pager } from 'gridsome'
export default {
  components: {
    Pager
  },
  metaInfo: {
    title: 'Hello, world!'
  }
}
</script>

<style scoped>
.home-links a {
  margin-right: 1rem;
}

.pager-container {
  display: inline-block;
  font-size: 1rem;
  text-align: center;
  width: 100%;
  color: black;
}
  
.pager-container__link {
    text-align: center;
    padding: 0.8rem 1.2rem;
    text-decoration: none;
    border: 1px solid rgb(220,220,220);
    border-radius: 50%;
    margin: 2px;
}

.active {
  background-color:  rgb(231,172,207);
  border-radius: 50%;
  border: none;
}

</style>
