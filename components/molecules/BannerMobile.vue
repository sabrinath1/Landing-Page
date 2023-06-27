<script setup lang="ts">
const props = defineProps<{
  imgMobile: string;
}>();
</script>
<template>
  <div
    :style="{ backgroundImage: `url(${props.imgMobile})` }"
    class="hero mb-20 block md:hidden"
  >
    <div class="text-end text-neutral-content h-[30rem] w-full px-5 sm:px-20">
      <div class="flex-col pt-16 w-72 justify-center text-center ml-32">
        <h1 class="mb-5 pl-4 text-3xl xl:text-7xl font-bold pt-28 text-primary">
          Sabrina Campos
        </h1>
        <h1 class="mb-5 px-6 text-2xl font-bold text-center flex-wrap pt-6">
          Advocacia e Assessoria Jurídica
        </h1>
      </div>

      <AtomsParagraph> </AtomsParagraph>
      <!-- <div class="sm:py-10 invisible sm:visible">
        <AtomsButtonContact
          ghost
          color="#a38a43"
          text-color="#ffffff"
          size="large"
        >
          Saber Mais
        </AtomsButtonContact>
      </div> -->
    </div>
  </div>
</template>
