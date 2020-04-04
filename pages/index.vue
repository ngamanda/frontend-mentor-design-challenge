<template>
  <div class="container">
    <h1 class="title">Hello</h1>
    <p class="subtitle">
      Here's my 16 page frontend practice from
      <a
        href="https://dev.to/frontendmentor/16-front-end-projects-with-designs-to-help-improve-your-coding-skills-5ajl?fbclid=IwAR0zBHiyoJXRedmp_NPaCuyBgHCGMTS7y3VSrKu10f7-QB9htmtdx-ieDN8"
        target="_blank"
      >Frontend&nbsp;Mentor</a>
    </p>
    <ol class="list">
      <li>
        <nuxt-link to="/challenge-1">Single price grid</nuxt-link>
      </li>
      <li>
        <nuxt-link to="/challenge-2">Four card feature</nuxt-link>
      </li>
      <li>
        <nuxt-link to="/challenge-3">Huddle landing page</nuxt-link>
      </li>
    </ol>
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: 'Frontend Mentor Challange | Amanda Ng'
    }
  }
}
</script>

<style scoped>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 60px;
  color: #35495e;
  letter-spacing: 1px;
  margin-bottom: 16px;
}

.subtitle {
  color: #526488;
  line-height: 1.5;
  padding-bottom: 15px;
}

a,
a:visited,
a:hover {
  text-decoration: none;
  color: #42b983;
}

.list {
  line-height: 2;
  padding-left: 20px;
}
</style>
