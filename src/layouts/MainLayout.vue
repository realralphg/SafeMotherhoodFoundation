<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar>
        <!-- <a href="/"><img src="logos/logo1240.png" alt="logo" style="height: 40px; max-width: 40px; padding-top: 5px;"></a> -->
        <q-icon name="bubble_chart" size="30px"/>
        

        <q-toolbar-title class="text-h6">
          <router-link to="/" tag="span" style="cursor: pointer"> SMF </router-link>
        </q-toolbar-title>

        <q-space/>

        <q-btn no-caps flat class="gt-xs row" color="grey-2" v-for="link in essentialLinks" :key="link.id" :to="link.to" exact clickable>
          <div class="column q-mr-md">
            <q-item-label>{{link.label}}</q-item-label>
          </div>
        </q-btn>  

        <q-btn
          class="button"
          flat
          dense
          round
          icon="menu"
          aria-label="Menu"
          @click="leftDrawerOpen = !leftDrawerOpen"
        />
      </q-toolbar>
    </q-header>

    <q-footer>
      <div class="text-center bg-grey-10">
        <div class="text-primary">Safe Motherhood Foundation</div>        
        <div class="text-grey-6">Copyright 2020</div>                
        <div class="text-grey-6">Greysoft Technologies</div>
      </div>
    </q-footer>

    <q-drawer
      v-model="leftDrawerOpen"
      :width="250"
      content-class="bg-primary"
    >
      <q-list>
        <q-item-label header class="text-white text-h5 text-weight-light">
          #SMF
        </q-item-label>

        <q-item class="text-grey-5" v-for="link in essentialLinks" :key="link.id" :to="link.to" exact clickable>
          <q-item-section avatar>
            <q-icon :name="link.icon"></q-icon>
          </q-item-section>

          <q-item-section>
            <q-item-label>{{link.label}}</q-item-label>
          </q-item-section>
        </q-item>

      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
export default {
  name: 'MainLayout',

  data () {
    return {
      leftDrawerOpen: false,

      essentialLinks: [
        {
          label: 'Home',
          icon: 'home',
          to: '/'
        },

        {
          label: 'About Us',
          icon: 'groups',
          to: '/about'
        },

        {
          label: 'Donate',
          icon: 'favorite',
          to: '/donate'
        },        

        {
          label: 'Contact Us',
          icon: 'phone',
          to: '/contact'
        },
      ]      
    }
  }
}
</script>

<style scoped>
@media (min-width: 600px){
  .button{
    display: none
  }
}

@media (max-width: 600px){
  #breadcrumbs{
    display: none
  }

  .toolbar-title{
    display: none
  }
}

.q-router-link--exact-active{
  color: white !important;
}

.fixed-bottom{
  position:absolute;
}

a{
    text-decoration: none;
    color: #26A69A;        
}

</style>