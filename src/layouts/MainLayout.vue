<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated class="">
      <q-toolbar class="bg-white text-brown">
        <!-- <a href="/"><img src="logos/logo1240.png" alt="logo" style="height: 40px; max-width: 40px; padding-top: 5px;"></a> -->
        <q-icon name="bubble_chart" size="30px" />

        <q-toolbar-title class="text-h6">
          <router-link to="/" tag="span" style="cursor: pointer">
            SMF
          </router-link>
        </q-toolbar-title>

        <q-space />

        <q-btn
          no-caps
          flat
          class="gt-xs row"
          color="grey-9"
          v-for="link in essentialLinks"
          :key="link.id"
          :to="link.to"
          exact
          clickable
        >
          <div class="column q-mr-md">
            <q-item-label>{{ link.label }}</q-item-label>
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
      <div class="q-pa-xl bg-black">
        <footer>
          <div class="row">
            <div class="col-md-6 col-sm-12 col-xs-12 q-pt-md">
              <div class="text-body1 typo1 my-font">
                © 2020 Safe Motherhood Foundation. All rights reserved.
              </div>
            </div>
            <div class="col-md-6 col-sm-12 col-xs-12">
              <div class="row">
                <div class="col-md-4 col-sm-12 col-xs-12 q-pt-md my-font-nav">
                  <div class="text-body1 typo1 text-bold my-font">
                    NAVIGATION
                  </div>
                  <div class="text-body1 typo1 q-mt-md cursor-pointer">
                    Home
                  </div>
                  <div class="text-body1 typo1 q-mt-md cursor-pointer">
                    About Us
                  </div>
                  <div class="text-body1 typo1 q-mt-md cursor-pointer">
                    Donate
                  </div>
                  <div class="text-body1 typo1 q-mt-md cursor-pointer">
                    Contact Us
                  </div>
                </div>
                <div class="col-md-4 col-sm-12 col-xs-12 q-pt-md my-font-nav">
                  <div class="text-body1 typo1 text-bold my-font">LEGAL</div>
                  <div class="text-body1 typo1 q-mt-md cursor-pointer">
                    Terms and Agreement
                  </div>
                  <div class="text-body1 typo1 q-mt-md cursor-pointer">
                    Privacy Policy
                  </div>
                </div>
                <div class="col-md-4 col-sm-12 col-xs-12 q-pt-md my-font-nav">
                  <div class="text-body1 typo1 text-bold my-font">CONNECT</div>
                  <div class="text-body1 typo1 q-mt-md">
                    support@sfm.com
                  </div>
                  <div class="text-body1 typo1 q-mt-md">+234 805 555 5555</div>
                </div>
              </div>
            </div>
          </div>
        </footer>
      </div>
      <!-- <div class="text-center bg-grey-10">
        <div class="text-primary">Safe Motherhood Foundation</div>
        <div class="text-grey-6">Copyright 2020</div>
        <div class="text-grey-6">Greysoft Technologies</div>
      </div> -->
    </q-footer>

    <!-- <q-drawer v-model="leftDrawerOpen" :width="250" content-class="bg-primary">
      <q-list>
        <q-item-label header class="text-white text-h5 text-weight-light">
          #SMF
        </q-item-label>

        <q-item
          class="text-grey-5"
          v-for="link in essentialLinks"
          :key="link.id"
          :to="link.to"
          exact
          clickable
        >
          <q-item-section avatar>
            <q-icon :name="link.icon"></q-icon>
          </q-item-section>

          <q-item-section>
            <q-item-label>{{ link.label }}</q-item-label>
          </q-item-section>
        </q-item>
      </q-list>
    </q-drawer> -->

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
export default {
  name: "MainLayout",

  data() {
    return {
      leftDrawerOpen: false,

      essentialLinks: [
        {
          label: "Home",
          icon: "home",
          to: "/"
        },

        {
          label: "About Us",
          icon: "groups",
          to: "/about"
        },

        {
          label: "Donate",
          icon: "favorite",
          to: "/donate"
        },

        {
          label: "Contact Us",
          icon: "phone",
          to: "/contact"
        }
      ]
    };
  }
};
</script>

<style scoped>
@media (min-width: 600px) {
  .button {
    display: none;
  }
}

@media (max-width: 600px) {
  #breadcrumbs {
    display: none;
  }

  .toolbar-title {
    display: none;
  }
}

.q-router-link--exact-active {
  color: white !important;
}

.fixed-bottom {
  position: absolute;
}

a {
  text-decoration: none;
  color: #26a69a;
}
</style>
