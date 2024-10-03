<script setup lang="ts">
// import TheWelcome from '../components/TheWelcome.vue'

import { useScreenOrientation, useWindowSize } from '@vueuse/core'
import { computed } from 'vue';

const {
  isSupported,
  orientation,
  angle,
  lockOrientation,
  unlockOrientation,
} = useScreenOrientation()

const screenWidth = computed(() => {
    return screen.width;
});
const screenHeight = computed(() => {
    return screen.height;
});
const outerWidth = computed(() => {
    return window.outerWidth;
});
const outerHeight = computed(() => {
    return window.outerHeight;
});
const innerWidth = computed(() => {
    return window.innerWidth;
});
const innerHeight = computed(() => {
    return window.innerHeight;
});

const { width, height } = useWindowSize()

</script>

<template>
  <main>
    <p>
      Screen size: {{ screenWidth }} &#215; {{ screenHeight }}
    </p>
    <p>
      Outer window: {{ outerWidth }} &#215; {{ outerHeight }}
    </p>
    <p>
      Inner window: {{ innerWidth }} &#215; {{ innerHeight }}
    </p>
    <p>
      Orientation type: {{ orientation }}
    </p>
    <p>

    </p>
    <!-- <TheWelcome /> -->
  </main>
</template>
