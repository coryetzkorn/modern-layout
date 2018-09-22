<template>
  <div class="layout">
    <div></div>
  </div>
</template>

<script>
export default {
  name: "CenterCenter",
  props: {
    name: String
  }
}
</script>

<style scoped>
.layout {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 240px;
}
.layout div {
  width: 100px;
  height: 100px;
  background: orange;
}
</style>
