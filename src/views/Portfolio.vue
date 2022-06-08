<template>
  <v-container>
    <v-row>

      <v-col v-for="(item, index) in portfolio" lg="6" xl="6">

        <router-link class="rtl" :to="'/portfolio/'+index">

          <span>{{item.title}}</span>
          <!--CARD-->
        </router-link>
      </v-col>


    </v-row>
  </v-container>
</template>

<script>
import Portfolio from '../assets/portfolio.json'


export default ({
  name: 'Portfolio',
  data(){
    return{
      portfolio: Portfolio,
    }
  }
});
</script>

<style>

</style>
