<script setup lang="ts">
const social = useSocialRedirect();
</script>
<template>
  <n-button text style="font-size: 30px" @click="social.redirect('linkedin')">
    <Icon
      name="mdi:linkedin"
      class="text-secondary hover:text-primarytransition-all"
    />
  </n-button>
</template>
