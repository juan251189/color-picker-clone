<template>
 <div class="colors-picker">
   <div class="color-block"

   v-for="(color,i) in colors" :key="i" :style="'background:'+color" @click="setColor(color)">

   </div>
 </div>

</template>


<script>

  export default{
    name:'color-picker',
    props: ['colors'],
    methods: {
      setColor(color) {
        this.$emit('setColor',color);


      }
    }
  }
</script>

<style media="screen">
  .colors-picker{
    display: grid;
      width: 125px;
      margin:15px auto;
      grid-template-columns: repeat(5,45px);

  }
  .color-block-picker{

    height: 25px;
  }
</style>
