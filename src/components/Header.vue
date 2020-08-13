<template>
  <header>
    <div class="header-text">
      Color<span class="span-header">Picker</span>
    </div>
    <div class="color-block" :style="'background:'+color">

    </div>

  </header>
</template>



<script>

  export default{
  name:'Nav-header',
  props: ['color']

  }
</script>
<style>

header{
  display:flex;
  background-color: black;
  justify-content: space-between;
  align-items: center;
  height: 110px;
  padding: 0 20px;
  margin: auto;

}

.header-text{
  color: white;
  font-weight: 900;
  font-size: 33px;
}
.span-header{
  color:rgb(196, 168, 46);
}
.color-block{
width: 40px;
height: 40px;
border: 1px dotted white;
}
</style>
