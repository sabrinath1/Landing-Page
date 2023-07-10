<script setup lang="ts">
const items = ref([
  {
    label: "Localização",
    content: "Av. Dr. Afonso Vergueiro, 1749 - Centro, Sorocaba",
    icon: "fa-solid fa-map-location-dot",
  },
  {
    label: "Contato",
    content: "(15)98155-0048",
    icon: "fa-brands",
  },
  {
    label: "E-mail",
    content: "sabrina@advocacia.com.br",
    icon: "",
  },
]);
</script>
<template>
  <div class="flex flex-col justify-center py-10 justify-items-center h-full">
    <div class="grid grid-cols-1 items-center w-full px-10 justify-center">
      <div>
        <div
          class="grid grid-cols-2 py-3 items-center justify-center"
          v-for="i in items"
        >
          <div
            class="flex justify-center md:justify-end items-center w-24 h-24 sm:w-24 sm:h-28 rounded-lg"
          >
            <!-- <font-awesome-icon class="text-base-100 text-4xl" :icon="i.icon" /> -->
          </div>
          <div>
            <h5 class="font-bold text-secondary">{{ i.label }}</h5>
            <p class="flex w-28 flex-wrap text-primary">{{ i.content }}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
