<template>
  <div class="layout">
    <div></div>
    <div></div>
    <div></div>
    <div></div>
    <div></div>
    <div></div>
    <div></div>
    <div></div>
    <div></div>
    <div></div>
    <div></div>
    <div></div>
    <div></div>
    <div></div>
    <div></div>
    <div></div>
  </div>
</template>

<script>
export default {
  name: "Grid",
  props: {
    name: String
  }
}
</script>

<style scoped>
.layout {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-gap: 10px;
  height: 100%;
}
.layout div {
  padding-top: 100%;
}
.layout div:nth-child(3n - 0) {
  background: #a4d2ee;
}
.layout div:nth-child(3n - 1) {
  background: #c93e37;
}
.layout div:nth-child(3n - 2) {
  background: #ffd700;
}
</style>
