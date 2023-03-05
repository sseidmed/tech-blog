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
  background-color: #f3f7f9;
  color: black;
}
.header {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: 100px;
  height: 200px;
}
.nav__link {
  margin-left: 20px;
}

</style>
