<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar class="row">
        <div class=" col-11 flex ">
          <q-btn flat dense round icon="menu" aria-label="Menu" @click="toggleLeftDrawer" />
          <q-input style="width:400px" dense rounded outlined v-model="searchText" label="Search" bg-color="white"><q-icon
              name="search" class="q-my-md" /></q-input>
        </div>
        <div class="row">
          <q-icon name="notifications" class=" q-my-md q-mr-md items-end" />
          <q-icon name="mode" class="q-my-md q-ml-md items-end" />
        </div>


      </q-toolbar>
    </q-header>

    <q-drawer v-model="leftDrawerOpen" show-if-above bordered>
      <div class="flex flex-center" style=" height:50px;font-size: 25px;">
        admin kit
      </div>
      <q-list bordered class="">
        <EssentialLink v-for="link in essentialLinks" :key="link.title" v-bind="link" />
      </q-list>
    </q-drawer>

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
  name: 'MainLayout',

  components: {
    EssentialLink
  },

  setup() {
    const leftDrawerOpen = ref(false)

    return {
      essentialLinks: linksList,
      leftDrawerOpen,
      toggleLeftDrawer() {
        leftDrawerOpen.value = !leftDrawerOpen.value
      }
    }
  }
})
</script>
