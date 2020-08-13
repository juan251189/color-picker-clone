<template>
  <div id="app">
    <Header :color="color"></Header>
    <ColorPicker :colors="colors" @setColor="setColor"></ColorPicker>
    <ColorGrid :color="color"></ColorGrid>
  </div>
</template>

<script>
import Header from '@/components/Header';
import ColorPicker from '@/components/Color-Picker';
import ColorGrid from '@/components/ColorGrid';
export default {
  name: 'App',
  components: {
    Header,
    ColorPicker,
    ColorGrid
  },
  data(){
    return{
      colors:['#c23611','#961e35','#f66092','#06470a','#146fd5'],
      color:''
    }
  },
  methods:{
    setColor(color){
      this.color=color;
    }
  }
}
</script>

<style>

body{
  margin: 0;
  padding: 0;
}
</style>
