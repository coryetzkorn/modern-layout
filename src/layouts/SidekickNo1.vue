<template>
  <div class="layout">
    <div></div>
    <div></div>
  </div>
</template>

<script>
export default {
  name: "SidekickNo1",
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
  background: #715c7c;
}
.layout div:nth-child(2) {
  background: #4c8438;
  flex-grow: 3;
}
</style>
