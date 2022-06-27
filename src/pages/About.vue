<template>
  <Layout>
    <h1>About me</h1>
    <footer>
      <div class="author">
        <img src="../../static/glasses.png" alt="" width="50px" height="50px"><p>Author: Shay Seidmedova</p>
      </div>
      <p class="home-links">
        <a href="https://www.linkedin.com/in/shahlo-seidmedova/" target="_blank" rel="noopener"><img src="../../static/linkedin.png" alt="linkedin link" width="30px" height="30px"></a>
        <a href="https://github.com/sseidmed" target="_blank" rel="noopener"><img src="../../static/github.png" alt="github link" width="30px" height="30px"></a>
        <a href="mailto:sseidmed@gmail.com"><img src="../../static/email.png" alt="" width="30px" height="30px"></a>
      </p>
      <!-- <div class="email">
        <img src="../../static/email.png" alt="" width="50px" height="50px"><p><a href="mailto:sseidmed@gmail.com">sseidmed@gmail.com</a></p>
      </div> -->
      
    </footer>
    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Error doloremque omnis animi, eligendi magni a voluptatum, vitae, consequuntur rerum illum odit fugit assumenda rem dolores inventore iste reprehenderit maxime! Iusto.</p>
  </Layout>
</template>

<script>
export default {
  metaInfo: {
    title: 'About us'
  }
}
</script>

<style scoped>
footer {
  display: flex;
  justify-content: space-between;
  padding: 0px 5px 0px 5px;
  max-width: 760px;
  background-color: rgb(231,172,207);
  color: #fff;
  max-height: 60px;
}

.author {
  display: flex;
}

.home-links > a {
  margin: 5px;
}
</style>
