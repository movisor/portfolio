<template>
  <div class="">
     <span class="snippet"> {{project.snippet}} </span>
    <h1>
    {{project.title}}
    </h1>
  </div>
</template>

<script>
import Portfolio from '../assets/portfolio.json';



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
.snippet{
  color:white;
}
</style>
