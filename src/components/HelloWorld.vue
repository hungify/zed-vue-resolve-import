<script setup lang="ts">
interface Slots {
  default: (props: { default: string }) => string
  top: (props: { top: number }) => string
  bottom: (props: { bottom: boolean }) => string
}

defineSlots<Slots>()
</script>

<template>
  <div class="greetings">
    <slot name="default" default="1">
      <p>default</p>
    </slot>

    <slot name="top" :top="1">
      <p>Top</p>
    </slot>

    <slot name="bottom" bottom>
      <p>bottom</p>
    </slot>
  </div>
</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  position: relative;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>
