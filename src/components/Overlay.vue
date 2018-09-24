<template>
  <div class="overlay">
    <div class="overlay__panel overlay__panel--left">
      <div class="overlay__align">
        <Card v-bind:layout="layout" v-bind:show-label="false"/>
        <pre>
        </pre>
      </div>
    </div>
    <div class="overlay__panel overlay__panel--right">
      <div class="close" v-on:click="closeOverlay">Close</div>
      <div>
        <h2>{{ layout }}</h2>
      </div>
    </div>
  </div>
</template>

<script>
import Card from "./Card.vue"

export default {
  name: "Overlay",
  components: {
    Card
  },
  props: {
    layout: String
  },
  data: function() {
    return {
      layoutHTML: ""
    }
  },
  mounted: function() {
    console.log(this.$refs)
    this.layoutHTML = "Coming Soon"
  },
  methods: {
    closeOverlay: function() {
      this.$emit("close-overlay")
    }
  }
}
</script>

<style scoped>
.overlay {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  display: flex;
}
.close {
  position: absolute;
  top: 30px;
  right: 30px;
  cursor: pointer;
}
.overlay__panel {
  width: 50%;
  display: flex;
  text-align: center;
  align-items: center;
  justify-content: center;
}
.overlay__align {
  width: 50%;
}
.overlay__panel--left {
  background: #ffffff;
}
.overlay__panel--left .card {
  width: 100%;
}
.overlay__panel--right {
  background: #000000;
  color: #ffffff;
}
.overlay__panel--right h2 {
  font-family: "GT America Trial", Helvetica, Arial, sans-serif;
  font-size: 60px;
  font-weight: 400;
  margin: 0;
}
pre {
  background: #f4f4f4;
  border-radius: 4px;
  padding: 20px;
}
</style>
