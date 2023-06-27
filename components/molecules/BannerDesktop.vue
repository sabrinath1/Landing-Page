<script setup lang="ts">
const props = defineProps<{
  imgDesktop: string;
}>();
</script>
<template>
  <div
    :style="{ backgroundImage: `url(${props.imgDesktop})` }"
    class="mb-20 hidden md:block sm:bg-left lg:bg-center"
  >
    <div
      class="text-center lg:text-end text-neutral-content h-[30rem] w-full px-20"
    >
      <div class="flex-col pt-10">
        <h1
          class="mb-5 text-6xl xl:text-7xl font-bold pt-24 lg:pt-20 text-star items-center lg:mt-10"
        >
          Advocacia e
        </h1>
        <h3 class="mb-5 text-6xl font-bold text-star">Assessoria Jurídica</h3>
      </div>

      <!-- <div class="sm:py-10 invisible sm:visible">
        <AtomsButtonContact @click="() => router.push('/about')">
          
        </AtomsButtonContact>
      </div> -->
    </div>
  </div>
</template>
