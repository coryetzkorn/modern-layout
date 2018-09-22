<template>
  <div class="card">
    <div class="card__layout">
      <Grid v-if='layout=="Grid"'/>
      <Columns v-if='layout=="Columns"'/>
      <SidekickNo1 v-if='layout=="Sidekick No. 1"'/>
      <SidekickNo2 v-if='layout=="Sidekick No. 2"'/>
      <CenterCenter v-if='layout=="Center Center"'/>
      <HotDog v-if='layout=="Hot Dog"'/>
      <Square v-if='layout=="Square"'/>
    </div>
    <div class="card__name">{{ layout }}</div>
  </div>
</template>

<script>
import Grid from "../layouts/Grid.vue"
import Columns from "../layouts/Columns.vue"
import SidekickNo1 from "../layouts/SidekickNo1.vue"
import SidekickNo2 from "../layouts/SidekickNo2.vue"
import CenterCenter from "../layouts/CenterCenter.vue"
import HotDog from "../layouts/HotDog.vue"
import Square from "../layouts/Square.vue"

export default {
  name: "Card",
  components: {
    Grid,
    Columns,
    SidekickNo1,
    SidekickNo2,
    CenterCenter,
    HotDog,
    Square
  },
  props: {
    layout: String
  }
}
</script>

<style scoped>
.card {
  background: #ffffff;
  cursor: pointer;
  position: relative;
}
.card__layout {
  position: absolute;
  top: 0;
  right: 0;
  left: 0;
  height: calc(100% - 38px);
}
.card::before {
  content: "";
  display: block;
  margin-top: 100%;
}
.card__name {
  font-family: "GT America Mono Trial", Helvetica, Arial, sans-serif;
  font-size: 14px;
  padding: 15px 0 5px 0;
  text-align: left;
}
</style>
