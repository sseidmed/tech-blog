<template>
  <Layout>
    <div class="about">
      <h1>About me</h1>
      <p class="home-links">
        <a href="https://www.linkedin.com/in/shahlo-seidmedova/" target="_blank" rel="noopener"><img src="../../static/linkedin.png" alt="linkedin link" width="30px" height="30px"></a>
        <a href="https://github.com/sseidmed" target="_blank" rel="noopener"><img src="../../static/github.png" alt="github link" width="30px" height="30px"></a>
        <!-- <a href="mailto:sseidmed@gmail.com"><img src="../../static/email.png" alt="" width="30px" height="30px"></a> -->
      </p>
      <p>I am a junior developer at Relevize (channel partner marketing platform). 
        I work with Vue.js and Flask. 
        I like to learn new tools and technologies whenever I can. I am also an avid reader, 
        especially books on productivity and self-improvement.<br>
        <p><i>This blog was built with Gridsome and hosted on Netlify.</i></p>
      </p>
    </div>
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
/* footer {
  display: flex;
  justify-content: space-between;
  padding: 0px 5px 0px 5px;
  max-width: 760px;
  color: #fff;
  max-height: 60px;
} */

.home-links > a {
  margin: 5px;
}
.about {
  display: flex;
  flex-direction: column;
  flex-wrap: wrap;
  width: 50%;
  justify-content: center;
  margin: auto;
}

.about > * {
  width: 100%;
}
</style>
