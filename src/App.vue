<script setup lang="ts">
import HelloWorld from './components/HelloWorld.vue'
import ReHelloWorld from './components/ReHelloWorld.vue'
</script>

<template>
  <!-- <HelloWorld>
    <template #default="item">
      <h1 >{{ item }}</h1>
    </template>
  </HelloWorld>
  <br /> -->

  <ReHelloWorld>
    <template #default="item">
      <h1>{{ item }}</h1>
    </template>
  </ReHelloWorld>
</template>
