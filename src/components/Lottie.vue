<template>
  <div :style="style" ref="lavContainer"></div>
</template>

<script>
/* eslint-disable @typescript-eslint/no-unsafe-assignment */
/* eslint-disable @typescript-eslint/no-unsafe-member-access */
/* eslint-disable @typescript-eslint/restrict-template-expressions */
import lottie from 'lottie-web'

export default {
  props: {
    src: String,
    height: Number,
    width: Number,
    loop: {
      type: Boolean,
      default: true
    },
    autoplay: {
      type: Boolean,
      default: true
    },
    speed: {
      type: Number,
      default: 1
    },
    rendererSettings: Object
  },
  data() {
    return {
      style: {
        width: this.width ? `${this.width}px` : '100%',
        height: this.height ? `${this.height}px` : '100%',
        overflow: 'hidden',
        margin: '0'
      }
    }
  },
  mounted() {
    this.anim = lottie
      .loadAnimation({
        container: this.$refs.lavContainer,
        renderer: 'svg',
        loop: this.loop,
        autoplay: this.autoplay,
        path: this.src,
        rendererSettings: this.rendererSettings
      })
      .setSpeed(this.speed)
  }
}
</script>
