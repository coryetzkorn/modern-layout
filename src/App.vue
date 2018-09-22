<template>
  <div id="app">
    <div class="title">
      <div class="title__inner">
        <h1>Modern Layout</h1>
        <p>A collection of CSS layouts built with flexbox and grid.<br>No floats. Just a few divs. By <a href="https://www.coryetzkorn.com">@coryetzkorn</a>.</p>
      </div>
    </div>
    <div class="cards">
      <Card layout="Grid"/>
      <Card layout="Columns"/>
      <Card layout="Sidekick No. 1"/>
      <Card layout="Sidekick No. 2"/>
      <Card layout="Grid"/>
      <Card layout="Center Center"/>
      <Card layout="Sidekick No. 1"/>
      <Card layout="Sidekick No. 2"/>
      <Card layout="Grid"/>
      <Card layout="Columns"/>
      <Card layout="Sidekick No. 1"/>
      <Card layout="Sidekick No. 2"/>
      <Card layout="Grid"/>
      <Card layout="Columns"/>
      <Card layout="Sidekick No. 1"/>
      <Card layout="Sidekick No. 2"/>
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
  padding: 0 20px;
}
.title {
  margin: 8em 40px;
}
.title h1 {
  font-size: 100px;
  font-weight: 400;
  margin: 0;
}
.title p {
  font-family: "GT America Trial", Helvetica, Arial, sans-serif;
  font-size: 30px;
}
.title a {
  text-decoration: underline;
  color: #000;
}
.cards {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-gap: 40px;
  padding: 40px;
}
</style>
