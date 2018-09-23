<template>
  <div id="app">
    <div class="share">
      <a class="github-button" href="https://github.com/coryetzkorn/modern-layout" data-icon="octicon-star" data-size="large" data-show-count="true" aria-label="Star coryetzkorn/modern-layout on GitHub">Star</a>
    </div>
    <header class="header">
      <div class="header__inner">
        <h1>Modern Layout</h1>
        <p>A collection of CSS layouts built with flexbox and grid.<br>No floats or classes. Just a few divs. By <a href="https://www.coryetzkorn.com">@coryetzkorn</a>.</p>
      </div>
    </header>
    <div class="cards">
      <Card layout="Grid" v-on:open-overlay="openOverlay"/>
      <Card layout="Columns" v-on:open-overlay="openOverlay"/>
      <Card layout="Sidekick No. 1" v-on:open-overlay="openOverlay"/>
      <Card layout="Sidekick No. 2" v-on:open-overlay="openOverlay"/>
      <Card layout="Hot Dog" v-on:open-overlay="openOverlay"/>
      <Card layout="Square" v-on:open-overlay="openOverlay"/>
      <Card layout="Center Center" v-on:open-overlay="openOverlay"/>
      <Card layout="Sidekick No. 1" v-on:open-overlay="openOverlay"/>
      <Card layout="Sidekick No. 2" v-on:open-overlay="openOverlay"/>
      <Card layout="Columns" v-on:open-overlay="openOverlay"/>
      <Card layout="Grid" v-on:open-overlay="openOverlay"/>
      <Card layout="Center Center" v-on:open-overlay="openOverlay"/>
      <Card layout="Hot Dog" v-on:open-overlay="openOverlay"/>
      <Card layout="Square" v-on:open-overlay="openOverlay"/>
      <Card layout="Grid" v-on:open-overlay="openOverlay"/>
      <Card layout="Columns" v-on:open-overlay="openOverlay"/>
      <Card layout="Sidekick No. 1" v-on:open-overlay="openOverlay"/>
      <Card layout="Sidekick No. 2" v-on:open-overlay="openOverlay"/>
      <Card layout="Hot Dog" v-on:open-overlay="openOverlay"/>
      <Card layout="Center Center" v-on:open-overlay="openOverlay"/>
      <Card layout="Sidekick No. 1" v-on:open-overlay="openOverlay"/>
      <Card layout="Sidekick No. 2" v-on:open-overlay="openOverlay"/>
      <Card layout="Columns" v-on:open-overlay="openOverlay"/>
      <Card layout="Square" v-on:open-overlay="openOverlay"/>
      <Card layout="Grid" v-on:open-overlay="openOverlay"/>
      <Card layout="Center Center" v-on:open-overlay="openOverlay"/>
      <Card layout="Hot Dog" v-on:open-overlay="openOverlay"/>
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
    <div class="overlay" v-if="activeLayout">
      <div class="overlay__panel">
        <Card v-bind:layout="activeLayout" v-bind:show-label="false"/>
      </div>
      <div class="overlay__panel">
        <div class="close" v-on:click="closeOverlay">Close</div>
        <div>
          <h2>{{ activeLayout }}</h2>
        </div>
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
  },
  data: function() {
    return {
      activeLayout: ""
    }
  },
  methods: {
    openOverlay: function(layout) {
      this.activeLayout = layout
    },
    closeOverlay: function() {
      this.activeLayout = ""
    }
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

.overlay {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  display: flex;
}
.overlay__panel {
  width: 50%;
  display: flex;
  text-align: center;
  align-items: center;
  justify-content: center;
}
.overlay__panel:nth-child(1) {
  background: #ffffff;
}
.overlay__panel:nth-child(1) .card {
  width: 50%;
}
.overlay__panel:nth-child(2) {
  background: #000000;
  color: #ffffff;
}
.overlay__panel:nth-child(2) h2 {
  font-family: "GT America Trial", Helvetica, Arial, sans-serif;
  font-size: 60px;
  font-weight: 400;
  margin: 0;
}

.share {
  text-align: right;
  flex-grow: 1;
  padding-top: 30px;
  position: absolute;
  top: 0;
  right: 50px;
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
