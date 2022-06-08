<template>
  <v-app>
    <v-main>

      <!--SIDEBAR-->
      <v-navigation-drawer>
        test
      </v-navigation-drawer>
      <!--END SIDEBAR-->


      <v-content>
      <!--ROUTER VIEW-->

      <router-view />

      <!--END ROUTER VIEW-->
      </v-content>


      <v-bottom-navigation v-model="value" class="bottom_menu">
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
    </v-main>
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