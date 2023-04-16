<template>
  <Layout>
    <ul class="posts">     
      <div v-for="post in $page.posts.edges" :key="post.id" class="individual-post">
        <g-link :to="post.node.path">
          <div class="post-title">
              {{ post.node.title}}          
          </div>
          <div class="date">{{ post.node.date }}</div>
        </g-link>
      </div>
    </ul>
    <Pager :info="$page.posts.pageInfo" class="pager-container"
       linkClass="pager-container__link" showLinks/>

  </Layout>
</template>

<page-query>

query Posts ($page: Int) {
  posts: allPost (perPage: 9, page: $page) @paginate {
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
        date (format: "D MMMM YYYY")
        description
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
    title: 'Tech blog'
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

.posts {
  display: flex;
  margin: auto;
  flex-wrap: wrap;
  justify-content: space-around;
  row-gap: 40px;
  width: 80%;
  margin-bottom: 150px;
}
.individual-post {
  align-items: center;
  background-color: #dbe1e5;
  border-radius: 5px;
  box-sizing: border-box;
  color: inherit;
  display: flex;
  flex-direction: column;
  height: 345px;
  width: 30%;
  justify-content: flex-start;
  padding: 35px 35px 0;
  position: relative;
  box-shadow: rgba(17, 17, 26, 0.05) 0px 1px 0px, rgba(17, 17, 26, 0.1) 0px 0px 8px;
}

.post-title {
    font-family: "Roboto", sans-serif;
    font-size: 24px;
    margin-top: 22px;
}
.date {
  float: right;
  font-size: 15px;
}

</style>
