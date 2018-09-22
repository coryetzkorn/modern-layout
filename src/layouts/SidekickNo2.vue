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
  height: 100%;
  margin: 0 -5px;
}
.layout div {
  height: 100%;
  flex: 1 1 auto;
  margin: 0 5px;
}
.layout div:nth-child(1) {
  background: #59595b;
  flex-grow: 3;
}
.layout div:nth-child(2) {
  background: #a4d2ee;
}
</style>
