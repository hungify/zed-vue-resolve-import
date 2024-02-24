<script setup lang="ts">
import { ref, useSlots } from 'vue'
import HelloWorld from './HelloWorld.vue'

interface Slots {
  default: (props: { default?: string }) => string
  top: (props: { top?: number }) => string
  bottom: (props: { bottom?: boolean }) => string
}

defineSlots<Slots>()
const msg = ref('hello')
</script>

<template>
  <HelloWorld>
    <template v-for="(_, name) in $slots as unknown as Readonly<Slots>" #[name]="slotProps">
      <slot :name="name" v-bind="slotProps" />
    </template>
  </HelloWorld>
</template>
