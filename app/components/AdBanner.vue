<!-- components/AdsBanner.vue -->
<template>
  <ins
    class="adsbygoogle"
    style="display:block"
    data-ad-client="ca-pub-XXXXXXXXXXXXXXXX"
    data-ad-slot="XXXXXXXXXX"
    data-ad-format="auto"
    data-full-width-responsive="true"
  />
</template>

<script setup>
import { onMounted } from 'vue'

onMounted(() => {
  if (typeof window !== 'undefined' && window.adsbygoogle) {
    (window.adsbygoogle = window.adsbygoogle || []).push({})
  }
})
</script>
