<template>
  <div class="layout">
    <div class="sidebar"></div>
    <div class="main"></div>
  </div>
</template>

<script>
export default {
  name: "SidekickNo2",
  props: {
    name: String
  }
}
</script>

<style scoped>
.layout {
  display: flex;
  justify-content: space-between;
}
.sidebar {
  width: calc(75% - 10px);
  height: 190px;
  background: blue;
}
.main {
  width: calc(25% - 10px);
  height: 190px;
  background: red;
}
</style>
