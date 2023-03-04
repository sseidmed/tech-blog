<template>
  <div class="layout">
    <header class="header">
      <strong>
        <g-link to="/" class="logo">
          <img src="../../static/developer.png" alt="" width="100px" height="100px">
          <p class="blog-name">{{ $static.metadata.siteName }}</p>
        </g-link>
      </strong>
      <nav class="nav">
        <g-link class="nav__link" to="/">Blog</g-link>
        <g-link class="nav__link" to="/about/">About</g-link>
      </nav>
    </header>
    <hr>
    <slot/>
  </div>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<style>
body {
  font-family: -apple-system,system-ui,BlinkMacSystemFont,"Segoe UI",Roboto,"Helvetica Neue",Arial,sans-serif;
  margin:0;
  padding:0;
  line-height: 1.5;
}

.layout {
  max-width: 760px;
  margin: 0 auto;
  padding-left: 20px;
  padding-right: 20px;
}

.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
  height: 100px;
  padding: 5px;
}

.nav__link {
  margin-left: 20px;
}

.logo {
  display: flex;
}

.blog-name {
  display: flex;
  flex-direction: column;
  justify-content: center;
  margin-left: 10px;
}

</style>
