<template>
  <div class="layout">
    <div></div>
    <div></div>
    <div></div>
  </div>
</template>

<script>
export default {
  name: "HotDog",
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
.layout div:nth-child(1),
.layout div:nth-child(3) {
  background: #ffd700;
}
.layout div:nth-child(2) {
  background: #c93e37;
  flex-grow: 2;
}
</style>
