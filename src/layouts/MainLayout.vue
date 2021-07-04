<template>
  <q-layout view="lHh Lpr lFf">
    <q-header class="bg-white text-grey-10" bordered>
      <q-toolbar class="constrain">
        <q-btn to="/camera" class="desktop-screen q-mr-sm" flat dense round size="18px" icon="eva-camera-outline" />
        <q-separator class="desktop-screen" spaced vertical />
        <q-toolbar-title class="text-grand-hotel text-bold">
          Vevantaphoto
        </q-toolbar-title>
        <q-btn to="/" class="desktop-screen" flat dense round size="18px" icon="eva-home-outline" />
      </q-toolbar>
    </q-header>

    <q-footer class="bg-white mobile-screen" bordered>

      <q-tabs
        class="text-grey-10"
        active-color="primary"
        indicator-color="transparent"
      >
        <q-route-tab
          to="/"
          icon="eva-home-outline"
        />
        <q-route-tab
          to="/camera"
          icon="eva-camera-outline"
        />
      </q-tabs>

    </q-footer>

    <q-page-container class="bg-grey-1">
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
    }
  }
}
</script>
<style lang="sass">
.q-toolbar
  @media (min-width: $breakpoint-sm-min)
    height: 77px
.q-toolbar__title
  font-size: 30px
  @media (max-width: $breakpoint-xs-max)
    text-align: center


.q-footer
  .q-tab__icon
    font-size: 30px
</style>
