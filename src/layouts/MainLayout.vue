<template>
  <q-layout view="hHh lpR fFf">

    <q-header elevated class="bg-primary text-white" height-hint="98">
      <q-toolbar>
        <q-toolbar-title style="color:black; text-align: center" >
          <!-- <q-avatar>
            <img src="https://cdn.quasar.dev/logo-v2/svg/logo-mono-white.svg">
          </q-avatar> -->
          Thunder Novels
        </q-toolbar-title>
      </q-toolbar>

      <q-tabs align="left" style="color:black;text-align: center">
        <q-route-tab to="/" label="Home" />
        <q-route-tab to="/novels" label="Novels" />
        <q-route-tab to="/contato" label="Contato" />
      </q-tabs>
    </q-header>

    <q-page-container >
      <router-view />
    </q-page-container>

  </q-layout>
</template>
