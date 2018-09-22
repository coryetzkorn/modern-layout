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
  background: #ffd7c6;
  height: 100%;
}
.layout div {
  width: 50%;
  height: 50%;
  background: #fd6e00;
}
</style>
