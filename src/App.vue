<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <q-layout view="hHh LpR lFf">
  
    <q-header elevated class="bg-dark text-white" height-hint="98">
      <q-toolbar>
        <q-toolbar-title>
          <!-- <q-avatar>
            <img src="">
          </q-avatar> -->
           MANAGE USERS
        </q-toolbar-title>
        <q-tabs align="left">
          <q-route-tab to="/" label="HOME" />
          <q-route-tab to="/about" label="ABOUT" />
        </q-tabs>
      </q-toolbar>
    </q-header>

    <q-page-container>
      <router-view />
    </q-page-container>

    <q-footer class="bg-grey-3 text-white">
      <q-toolbar>
        <q-toolbar-title>
          <!-- <q-avatar>
            <img src="">
          </q-avatar> -->
          <div align="right" style="color: black; font-size: small;">By Theerat Choktaweesad.</div>
        </q-toolbar-title>
      </q-toolbar>
    </q-footer>

  </q-layout>
</template>

<style scoped>

</style>
