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
}
.layout div {
  width: calc(25% - 10px);
  height: 190px;
  background: blue;
}
</style>
