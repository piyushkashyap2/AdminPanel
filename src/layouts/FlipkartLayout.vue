<template>
  <q-layout view="lHh Lpr lFf">
    <q-header>

      <q-toolbar class="justify-center row text-white">
        <div class="row items-center justify-center " style="width:900px">
          <div class="row col-xs-12 col-sm-8 col-md-6 q-pa-sm items-center justify-center q-gutter-sm"
            style="min-width:320px">
            <div>
              <img style="height:20px"
                src="https://static-assets-web.flixcart.com/fk-p-linchpin-web/fk-cp-zion/img/flipkart-plus_8d85f4.png" />
            </div>

            <q-input class="col" dense outlined v-model="searchText" label="Search" bg-color="white">
              <template v-slot:append> <q-icon name="search" /></template>
            </q-input>

          </div>

          <div class="row col-xs-12 col-sm-7 q-pa-sm col-md-6 items-center justify-between">

            <q-btn label="became a seller" text-color="white" flat unelevated @click=""></q-btn>
            <q-btn flat style="color: white" label="More" />
            <q-btn flat style="color: white" label="Cart" icon="local_grocery_store" />
            <q-btn label="Login" align="between" color="white" text-color="blue" unelevated @click="basic = true"></q-btn>
          </div>


        </div>
      </q-toolbar>
    </q-header>

    <q-dialog v-model="basic" full-height full-width>
      <div class="row justify-center">
        <div class="row bg-white" style="width:800px">

          <div class="bg-primary col-4">
            tdryzz
          </div>
          <div class="col">
            hdrh
          </div>


        </div>

      </div>
    </q-dialog>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { defineComponent, ref } from 'vue'
import EssentialLink from 'components/EssentialLink.vue'

const linksList = [
  {
    title: 'Dashboard',
    caption: '',
    icon: 'dashboard',
    link: ''
  },
  {
    title: 'Calender',
    caption: '',
    icon: 'calendar_month',
    link: ''
  },
  {
    title: 'Map',
    caption: '',
    icon: 'map',
    link: ''
  },
  {
    title: 'Widgets',
    caption: '',
    icon: 'widgets',
    link: ''
  },
  {
    title: 'Form Element',
    caption: '',
    icon: 'format_align_center',
    link: ''
  },
  {
    title: 'Charts',
    caption: '',
    icon: 'bar_chart',
    link: ''
  },
  {
    title: 'Tables',
    caption: '',
    icon: 'table_chart',
    link: ''
  },
  {
    title: 'Authentication',
    caption: '',
    icon: 'verified',
    link: ''
  },

]

export default defineComponent({
  name: 'FlipkartLayout',

  components: {
    EssentialLink
  },

  setup() {
    const leftDrawerOpen = ref(false)

    return {
      essentialLinks: linksList,
      leftDrawerOpen,
      basic: ref(false),
      toggleLeftDrawer() {
        leftDrawerOpen.value = !leftDrawerOpen.value
      }
    }
  }
})
</script>
