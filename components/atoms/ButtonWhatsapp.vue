<script setup lang="ts">
const social = useSocialRedirect();
</script>
<template>
  <n-button text style="font-size: 30px" @click="social.redirect('whatsapp')">
    <Icon
      name="mdi:whatsapp"
      class="text-primary hover:text-secondary transition-all"
    />
  </n-button>
</template>
