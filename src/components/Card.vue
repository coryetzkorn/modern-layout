<template>
  <div class="card" @click="openOverlay">
    <div class="card__spacer">
      <div class="card__layout">
        <Grid v-if='layout=="Grid"'/>
        <Columns v-if='layout=="Columns"'/>
        <SidekickNo1 v-if='layout=="Sidekick No. 1"'/>
        <SidekickNo2 v-if='layout=="Sidekick No. 2"'/>
        <CenterCenter v-if='layout=="Center Center"'/>
        <HotDog v-if='layout=="Hot Dog"'/>
        <Square v-if='layout=="Square"'/>
      </div>
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
    layout: String,
    showLabel: Boolean
  },
  methods: {
    openOverlay: function() {
      this.$emit("open-overlay", this.layout)
    }
  }
}
</script>

<style scoped>
.card {
  background: #ffffff;
  cursor: pointer;
  position: relative;
  transform: scale(1, 1);
}
.card:active {
  transform: scale(1.05, 1.05);
}
.card__spacer {
  position: relative;
}
.card__spacer::before {
  content: "";
  display: block;
  padding-top: 100%;
}
.card__layout {
  position: absolute;
  top: 0;
  right: 0;
  left: 0;
  bottom: 0;
}
.card__name {
  font-family: "GT America Mono Trial", Helvetica, Arial, sans-serif;
  font-size: 14px;
  padding: 15px 0 5px 0;
  text-align: left;
}
</style>
