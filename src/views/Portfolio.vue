<template>
  <v-container>
    <v-row>

      <v-col v-for="(item, index) in portfolio" cols="12" lg="6" xl="6">

        <router-link class="rtl" :to="'/portfolio/'+index">

          <ProjectBox :project="item"/>

        </router-link>
      </v-col>


    </v-row>
  </v-container>
</template>

<script>
import Portfolio from '../assets/portfolio.json';
import ProjectBox from '../components/ProjectBox.vue';



export default ({
  name: 'Portfolio',
  components: {
    ProjectBox,
  },
  data(){
    return{
      portfolio: Portfolio,
    }
  }
});
</script>

<style>

</style>
