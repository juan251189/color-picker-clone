<template>
<div class="grid">
  <div class="grid-block" v-for="(block,i) in blocks"
  :key="i"
  @click="setColor(i)"
  :style="'background:'+block.color">

  </div>
</div>
</template>

<script>
export default {
  name: 'color-grid',
  props: ['color'],
  data() {
    return {
      blocks: [],
      size: 100
    }
  },
  methods: {
    initGrid() {
      for (let i = 0; i < this.size; i++) {
        this.blocks.push({color:'#fff'});
      }
    },
    setColor(i){
      this.blocks[i].color=this.color;
    }
  },
  created() {
    this.initGrid();

  }
}
</script>


<style>

.grid{
  display: grid;


  grid-template-row:repeat(10,45px);
  grid-template-columns: repeat(10, 45px);
  border: 1px dotted grey;
justify-content: center;
  align-items:center;


}

.grid-block {
  display: grid;
  height:45px;
  width: 45px;


  grid-template-row:repeat(10,45px);
  grid-template-columns: repeat(10, 45px);
  border: 1px solid grey;}
  </style>
