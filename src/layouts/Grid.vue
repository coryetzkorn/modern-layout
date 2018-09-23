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
.layout div:nth-child(2n - 3) {
  background: #333333;
}
.layout div:nth-child(2n - 2) {
  background: #59595b;
}
</style>
