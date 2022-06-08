<template>
  <v-app>
    

      <!--SIDEBAR-->
      <v-navigation-drawer>
        test
      </v-navigation-drawer>
      <!--END SIDEBAR-->

      <v-app-bar app v-if="this.$route.name != 'home'">
      <!--HOME BUTTON ONLY IF $route != HOME-->
      {{this.$route.name}}
      </v-app-bar>


      <v-main>
      <!--ROUTER VIEW-->

      <router-view />

      <!--END ROUTER VIEW-->
      </v-main>


      <v-bottom-navigation class="bottom_menu">
        <router-link class="rtl" to="/portfolio">
          <v-btn >
            <span class="menu_item">PORTFOLIO</span>
          </v-btn>
        </router-link>
        <router-link class="rtl" to="/bio">
          <v-btn >
            <span class="menu_item">BIO</span>
          </v-btn>
        </router-link>
        <router-link class="rtl" to="/research">
          <v-btn >
            <span class="menu_item">Research</span>
          </v-btn>
        </router-link>
        <router-link class="rtl" to="/contact">
          <v-btn >
            <span class="menu_item">Contact</span>
          </v-btn>
        </router-link>
        <router-link class="rtl" to="/portfolio">
          <v-btn >
            <span class="menu_item">PORTFOLIO</span>
          </v-btn>
        </router-link>

        
      </v-bottom-navigation>
    
  </v-app>
</template>

<script>

export default {
  name: 'App',

  data: () => ({
    //
  }),
}
</script>


<style lang="scss">

.rtl{
  font-family: Helvetica;
    text-decoration: none;
    color: black;
    display: flex;
    justify-content: center;
    align-items: center;
    .menu_item{
      font-weight:bold;
    }
}

</style>