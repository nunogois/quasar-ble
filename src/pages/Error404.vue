<template>
  <div class="fullscreen text-center q-pa-md flex flex-center">
    <div>
      <h5 class="q-ma-sm">404 - Not Found.</h5>

      <q-btn class="q-mt-xl" to="/" label="Go Home" color="primary" />
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from '@vue/composition-api'

export default defineComponent({
  name: 'Error404'
})
</script>
