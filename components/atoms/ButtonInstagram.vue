<script setup lang="ts">
const social = useSocialRedirect();
</script>
<template>
  <n-button text style="font-size: 30px" @click="social.redirect('instagram')">
    <Icon
      name="mdi:instagram"
      class="text-primary hover:text-secondary transition-all"
    />
  </n-button>
</template>
