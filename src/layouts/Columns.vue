<template>
  <div class="layout">
    <div></div>
    <div></div>
    <div></div>
    <div></div>
  </div>
</template>

<script>
export default {
  name: "Columns",
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
  background: #ffd7c6;
}
.layout div:nth-child(2) {
  background: #d9bc9c;
}
.layout div:nth-child(3) {
  background: #aaaead;
}
.layout div:nth-child(4) {
  background: #59595b;
}
</style>
