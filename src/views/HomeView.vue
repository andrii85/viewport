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

const { width, height } = useWindowSize()

</script>

<template>
  <main>
    <p>
      Screen size: {{ screenWidth }} &#215; {{ screenHeight }}
    </p>
    <p>
      Window size: {{ width }} &#215; {{ height }}
    </p>
    <p>

    </p>
    <p>
      Orientation type: {{ orientation }}
    </p>
    <p>

    </p>
    <!-- <TheWelcome /> -->
  </main>
</template>
