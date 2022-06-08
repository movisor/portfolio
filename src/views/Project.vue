<template>
  <div class="">
    <div class="container_black"></div>
     <span class="snippet"> {{project.snippet}} </span>
    <h1>
    {{project.title}}
    </h1>
  </div>
</template>

<script>
import Portfolio from '../assets/portfolio.json'


export default ({
  name: 'project',
  props:['project'],
  data(){
    return{
      project : Portfolio[this.project]
    }
  }
});
</script>

<style scoped>
.container_black{
  background-color:black;
  position:fixed;
  top:0;
  bottom:0;
  left:0;
  right:0;
}
.snippet{
  color:white;
}
</style>
