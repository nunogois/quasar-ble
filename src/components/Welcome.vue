<template>
  <q-dialog
    :value="value"
    @hide="
      $emit('update:value', false)
      $emit('hide')
    "
    :persistent="!$q.platform.is.capacitor"
  >
    <q-card class="text-center q-py-md">
      <q-card-section>
        <div class="text-h6">Welcome to Quasar BLE!</div>
      </q-card-section>
      <q-card-section class="q-pt-none">
        <lottie src="lottie/ble.json" :height="200" />
        <div class="q-ma-md text-center">
          <q-btn
            type="a"
            no-caps
            label="Check it out on GitHub!"
            href="https://github.com/nunogois/quasar-ble"
            target="_blank"
            class="welcome-link"
            color="black"
            icon="fab fa-github"
          />
        </div>
        <div v-if="native_os && native_os.native">
          Since you're running the
          <q-icon :color="native_os.color" :name="native_os.icon" />
          {{ native_os.name }} app you are good to go!
        </div>
        <div v-else-if="native_os && !native_os.native">
          Even though you are opening the app on an
          <q-icon :color="native_os.color" :name="native_os.icon" />
          {{ native_os.name }} device, it seems you are not using the native
          app. Please install it and try again!
        </div>
        <div v-else>
          Unfortunately your device is not supported 😢
          <br />
          Please try again with an Android or iOS device.
        </div>
      </q-card-section>
      <q-card-actions align="center" v-if="$q.platform.is.capacitor">
        <q-btn label="Start" color="primary" v-close-popup />
      </q-card-actions>
    </q-card>
  </q-dialog>
</template>

<script lang="ts">
import { defineComponent } from '@vue/composition-api'

import Lottie from 'components/Lottie.vue'

export default defineComponent({
  components: { Lottie },
  props: {
    value: {
      type: Boolean,
      required: true
    }
  },
  computed: {
    native_os(): {
      name: string
      icon: string
      color: string
      native: boolean
    } | null {
      if (this.$q.platform.is.android)
        return {
          name: 'Android',
          icon: 'fab fa-android',
          color: 'light-green-6',
          native: this.$q.platform.is.capacitor as boolean
        }
      else if (this.$q.platform.is.ios)
        return {
          name: 'iOS',
          icon: 'fab fa-android',
          color: 'light-green-6',
          native: this.$q.platform.is.capacitor as boolean
        }

      return null
    }
  }
})
</script>

<style lang="sass">
.welcome-link
  text-decoration: none
  color: #2c8aff
</style>
