<template>
  <v-app>
  <!-- header toolbar -->
    <v-toolbar id="toolbar__wrapper" fixed>

    <!-- dropdown menu -->  
      <v-menu class="hidden-sm-and-up">
        <v-toolbar-items slot="activator">
          <v-icon dark>menu</v-icon>
        </v-toolbar-items>
        <v-list id="dropdown__menu">
          <v-list-tile class="dropdown__list" v-for="item in menuItems" :key="item.title" @click="">
            <v-list-tile-title v-text="item.title" class="dropdown__list--item" />
          </v-list-tile>
        </v-list>
      </v-menu>
    <!-- end dropdown menu -->

    <!-- left menu --> 
      <v-spacer></v-spacer>
      <v-toolbar-items class="hidden-xs-only" scroll-off-screen>
        <v-btn class="toolbar__item" :ripple="false" flat :to="item.link" v-for="item in menuItemsLeft" :key="item.title">
          {{ item.title }}
        </v-btn>
      </v-toolbar-items>    
    <!-- emd left menu --> 

    <!-- logo -->   
      <v-toolbar-title>
        <router-link to="/" tag="span" style="cursor:pointer" class="hidden-xs-only">EXCIETY</router-link>
      </v-toolbar-title>
    <!-- en logo menu --> 

    <!-- right menu -->   
      <v-toolbar-items class="hidden-xs-only">
        <v-btn class="toolbar__item" :ripple="false" flat :to="item.link" v-for="item in menuItemsRight" :key="item.title">
          {{ item.title }}
        </v-btn>
      </v-toolbar-items>
      <v-spacer></v-spacer>
    <!-- end right menu --> 

    <!-- mobile logo -->   
      <v-toolbar-items class="hidden-sm-and-up">
        <v-icon dark>wifi_tethering</v-icon>
      </v-toolbar-items> 
    <!-- end mobile logo --> 

    </v-toolbar>
  <!-- end header toolbar -->

  <!-- page content -->
    <main>
      <router-view></router-view>
    </main>
  <!-- end page content -->

  </v-app>
</template>

<script>
export default {
  name: 'App',
  data () {
    return {
      menuItems: [
        { title: 'About' },
        { title: 'Features' },
        { title: 'Ads' },
        { title: 'Login' }
      ],
      menuItemsLeft: [
        { title: 'About' },
        { title: 'Features' }
      ],
      menuItemsRight: [
        { title: 'Ads' },
        { title: 'Login' }
      ]
    }
  }
}
</script>

<style lang="scss">

  * {font-family: $comforta;}

  .toolbar__title {
    margin: 0 150px;
  }

  #toolbar__wrapper {
    background: rgba(255,255,255,0.8);
    text-transform: lowercase;

    .toolbar__item {
      color: #000;
      font-size: 14px;
      font-weight: 600;
      letter-spacing: 2px;
      margin: 0 10px;
      padding: 0px !important;
      width: 100px;

      .btn__content {}      
      .btn__content::before {opacity: 0;}
      &:hover {color: $orange;}
    }
  }

  .menu__content {
    border-radius: 0px;
    left: 0 !important;
    right: 0;
    top: 0 !important;
    min-width: 100% !important;
  }

  #dropdown__menu {
    background: #fff;
    padding: 0;

    .dropdown__list--item {
      color: #000;
      text-transform: lowercase;
    }
  }

</style>
