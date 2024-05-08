<template>
  <q-layout view="hHh lpR fFf">

    <q-header
      reveal
      bordered
      class="bg-primary text-white"
      height-hint="98"
    >
      <div class="row">
        <q-toolbar class="col-2">
          <q-toolbar-title>
            <q-avatar>
              <img src="https://cdn.quasar.dev/logo-v2/svg/logo-mono-white.svg">
            </q-avatar>
            Title
          </q-toolbar-title>
        </q-toolbar>

        <q-tabs align="left">
          <q-route-tab
            to="/page1"
            label="Page One"
          />
          <q-route-tab
            to="/page2"
            label="Page Two"
          />
          <q-route-tab
            to="/page3"
            label="Page Three"
          />
        </q-tabs>
      </div>
    </q-header>

    <q-page-container>
      <router-view />
    </q-page-container>

    <q-footer
      reveal
      elevated
      class="bg-grey-8 text-white px-sm"
    >

      <div class="container q-pa-lg">
        <a
          href=""
          class=""
        >部長信箱</a>
        <p class="q-mt-md">中華民國教育部 版權所有 © 2024 Ministry of Education, R.O.C. All rights reserved.®</p>
        <p>使用人次：{{ peopleCount }}</p>
      </div>

    </q-footer>

  </q-layout>
</template>

<script
  setup
  lang="ts"
>

import { ref } from 'vue'

defineOptions({
  name: 'MainLayout'
})

const peopleCount = ref(0)

</script>
