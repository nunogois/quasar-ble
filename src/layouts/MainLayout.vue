<template>
  <q-layout view="hHh LpR fFf">
    <q-header bordered>
      <q-toolbar>
        <q-toolbar-title>
          Quasar BLE
        </q-toolbar-title>

        <div>Quasar v{{ $q.version }} + Capacitor v3</div>
      </q-toolbar>
    </q-header>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>
