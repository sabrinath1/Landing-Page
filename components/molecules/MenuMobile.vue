<script setup lang="ts">
const social = useSocialRedirect();
</script>

<template>
  <div
    class="menu p-4 w-80 bg-secondary/60 backdrop-blur-sm text-base-content z-[100]"
  >
    <div class="flex justify-end">
      <AtomsButtonClose />
    </div>
    <div class="flex mt-10 justify-start">
      <MoleculesMenu />
    </div>
    <div class="flex my-10 justify-center">
      <AtomsButtonContact></AtomsButtonContact>
    </div>
    <div class="flex justify-center mb-8 space-x-6 md:order-last md:mb-0">
      <AtomsButtonInstagram />
      <AtomsButtonFacebook />
      <AtomsButtonLinkedin />
      <AtomsButtonWhatsapp />
    </div>
  </div>
</template>
