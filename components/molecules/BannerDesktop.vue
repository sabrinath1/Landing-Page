<script setup lang="ts">
const props = defineProps<{
  imgDesktop: string;
}>();
</script>
<template>
  <div
    :style="{ backgroundImage: `url(${props.imgDesktop})` }"
    class="hero mb-20 hidden md:block"
  >
    <div
      class="text-center sm:text-end text-neutral-content h-[30rem] w-full px-5 sm:px-20"
    >
      <div class="flex-col w-full pt-10 pt-5 sm:pt-20">
        <h1
          class="mb-5 text-5xl xl:text-7xl font-bold pt-20 text-star items-center lg:mt-10 text-secondary"
        >
          Sabrina Campos
        </h1>
        <h4 class="mb-5 text-3xl font-bold text-star flex-wrap">
          Advocacia e Assessoria Jurídica
        </h4>
        <!-- <div class="sm:py-10 invisible sm:visible flex justify-center">
          <AtomsButtonContact> Saber Mais </AtomsButtonContact>
        </div> -->
      </div>
    </div>
  </div>
</template>
