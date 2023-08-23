---
layout: home
---

<MonacoEditor />

<script setup>
import { defineAsyncComponent } from 'vue';
import { inBrowser } from 'vitepress';

const MonacoEditor = inBrowser
  ? defineAsyncComponent(() => import('./components/monaco.vue'))
  : () => null;
</script>
