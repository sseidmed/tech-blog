<template>
  <div class="layout">
    <header class="header">
      <strong>
        <g-link to="/" class="logo">
          <img src="../../static/developer.png" alt="" width="100px" height="100px">
        </g-link>
      </strong>
      <nav class="nav">
        <g-link class="nav__link" to="/">Blog</g-link>
        <g-link class="nav__link" to="/about/">About</g-link>
      </nav>
    </header>
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
  background-color: #1f364d;
}
.header {
  display: flex;
  flex-direction: column;
  align-items: center;
  height: 200px;
  background-color: #dbe1e5;
  margin-bottom: 30px;
}
.nav__link {
  margin-left: 20px;
}

</style>
