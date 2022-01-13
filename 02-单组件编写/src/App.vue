<template>
  <h1>App.vue</h1>
  <Home />
  <Component1 />
</template>

<script lang="ts">
import { defineComponent } from "@vue/runtime-core";
import Home from "./views/Home.vue";
import Component1 from "./components/component-1.vue";

export default defineComponent({
  components: { Home, Component1 },
})
</script>