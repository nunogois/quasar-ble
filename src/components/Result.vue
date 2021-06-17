<template>
  <q-expansion-item group="results">
    <template v-slot:header>
      <q-item-section>
        {{ result.localName || result.device.deviceId }}
      </q-item-section>
      <q-item-section side>
        <div class="row items-center">
          <q-icon name="fas fa-wifi" :color="signal_color" />
        </div>
      </q-item-section>
    </template>

    <q-card style="max-width: 100%">
      <q-card-section>
        {{ result }}
      </q-card-section>
    </q-card>
  </q-expansion-item>
</template>

<script lang="ts">
import { defineComponent, PropType } from '@vue/composition-api'

import { ScanResult } from '../../src-capacitor/node_modules/@capacitor-community/bluetooth-le'

export default defineComponent({
  computed: {
    signal_color(): string {
      const latency = this.result.rssi * -1
      console.log(latency)
      let color = 'red'

      if (latency < 70) color = 'green'
      else if (latency < 90) color = 'yellow'

      return color
    }
  },
  props: {
    result: {
      type: Object as PropType<ScanResult>,
      required: true
    }
  }
})
</script>
