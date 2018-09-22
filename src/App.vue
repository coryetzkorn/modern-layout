<template>
  <div id="app">
    <div class="share">
      <a class="github-button" href="https://github.com/coryetzkorn/modern-layout" data-icon="octicon-star" data-size="large" data-show-count="true" aria-label="Star coryetzkorn/modern-layout on GitHub">Star</a>
    </div>
    <header class="header">
      <div class="header__inner">
        <h1>Modern Layout</h1>
        <p>A collection of CSS layouts built with flexbox and grid.<br>No floats. Just a few divs. By <a href="https://www.coryetzkorn.com">@coryetzkorn</a>.</p>
      </div>
    </header>
    <div class="cards">
      <Card layout="Grid"/>
      <Card layout="Columns"/>
      <Card layout="Sidekick No. 1"/>
      <Card layout="Sidekick No. 2"/>
      <Card layout="Hot Dog"/>
      <Card layout="Center Center"/>
      <Card layout="Sidekick No. 1"/>
      <Card layout="Sidekick No. 2"/>
      <Card layout="Columns"/>
      <Card layout="Grid"/>
      <Card layout="Center Center"/>
      <Card layout="Hot Dog"/>
      <Card layout="Grid"/>
      <Card layout="Columns"/>
      <Card layout="Sidekick No. 1"/>
      <Card layout="Sidekick No. 2"/>
      <Card layout="Hot Dog"/>
      <Card layout="Center Center"/>
      <Card layout="Sidekick No. 1"/>
      <Card layout="Sidekick No. 2"/>
      <Card layout="Columns"/>
      <Card layout="Grid"/>
      <Card layout="Center Center"/>
      <Card layout="Hot Dog"/>
    </div>
    <div class="q-and-a">
      <div class="q-and-a__item">
        <strong>Q</strong>Is this a CSS framework?<br>
        <strong>A</strong>No. These are just tiny snippets of code you can copy-paste.
      </div>
      <div class="q-and-a__item">
        <strong>Q</strong>Is this a CSS framework?<br>
        <strong>A</strong>No. These are just tiny snippets of code you can copy-paste.
      </div>
    </div>
  </div>
</template>

<script>
import Card from "./components/Card.vue"

export default {
  name: "app",
  components: {
    Card
  }
}
</script>

<style>
body,
html {
  margin: 0;
  padding: 0;
}
#app {
  font-family: "GT America Trial", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: black;
  padding: 0 0;
}
@media screen and (min-width: 800px) {
  #app {
    padding: 0 20px;
  }
}
.share {
  text-align: right;
  flex-grow: 1;
  padding-top: 30px;
  position: absolute;
  top: 0;
  right: 30px;
}
.header {
  margin: 12vh 40px;
}
.header h1 {
  font-size: 100px;
  font-weight: 400;
  margin: 0;
}
.header p {
  font-family: "GT America Trial", Helvetica, Arial, sans-serif;
  font-size: 30px;
}
.header a {
  text-decoration: underline;
  color: #000;
}
.cards {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  grid-gap: 40px;
  padding: 40px;
}
@media screen and (min-width: 800px) {
  .cards {
    grid-template-columns: repeat(4, 1fr);
  }
}
@media screen and (min-width: 1400px) {
  .cards {
    grid-template-columns: repeat(6, 1fr);
  }
}
.q-and-a__item {
  margin: 100px 0;
  padding: 0 40px;
  font-family: "GT America Trial", Helvetica, Arial, sans-serif;
  font-size: 30px;
}
.q-and-a__item strong {
  display: inline-block;
  width: 60px;
}
</style>
