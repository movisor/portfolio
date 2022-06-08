<template>
  <v-app>
    

      <!--SIDEBAR-->
      <v-navigation-drawer v-model="drawer">
        <!--INSERT SOCIAL ICONS HERE-->
      </v-navigation-drawer>
      <!--END SIDEBAR-->

      <v-app-bar app v-if="this.$route.name != 'home'">
      <!--HOME BUTTON ONLY IF $route != HOME-->
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
      {{this.$route.name}}
      </v-app-bar>


      <v-main :class="this.$route.name == 'project' ? 'bg_black' : ''">
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
    drawer: null
    }),
}
</script>


<style lang="scss">
body{
  font-family:Helvetica;
  text-transform:uppercase;
}
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

.bg_black{
  background:black;
  color:white;
}

</style>