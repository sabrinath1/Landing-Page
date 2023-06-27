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
    <div
      class="text-center sm:text-start text-neutral-content h-[30rem] w-full px-5 sm:px-20"
    >
      <div class="flex-col w-1/2 pt-14">
        <h1 class="mb-5 text-4xl xl:text-7xl font-bold pt-28">
          Sabrina Campos
        </h1>
        <!-- <h1 class="mb-5 text-3xl xl:text-5xl font-bold text-star flex-wrap">
          Advocacia e Assessoria Jurídica
        </h1> -->
      </div>
    </div>
  </div>
</template>
