<script setup lang="ts">
const myList = ref([
  {
    title: "Sobre",
    items: [
      {
        label: "Quem Somos",
        href: "",
        icon: "",
      },
      {
        label: "Serviços",
        href: "",
        icon: "",
      },
      {
        label: "Contato",
        href: "",
        icon: "",
      },
    ],
  },

  {
    title: "Contatos",
    items: [
      {
        label: "(15)99999-9999",
        href: "",
        icon: "",
      },
      {
        label: "sabrina@advocacia.com.br",
        href: "",
        icon: "",
      },
      {
        label: "Av. Campolim, 1749 - Campolim, Sorocaba - SP",
        href: "",
        icon: "",
      },
    ],
  },
  {
    title: "Funcionamento",
    items: [
      {
        label: "Segunda á Sexta: ",
        href: "",
        icon: "",
      },
      {
        label: "09:00 ás 18:00 horas",
        href: "",
        icon: "",
      },
    ],
  },
]);
</script>

<template>
  <footer class="bg-primary" aria-labelledby="footer-heading ">
    <div class="px-4 py-12 mx-auto w-full sm:px-6 lg:px-16">
      <div class="xl:grid xl:grid-cols-3 xl:gap-8">
        <div class="flex flex-col justify-center items-center my-3">
          <img
            src="img/logotipo-vertical.png"
            alt="Logotipo VerticaL Sabrina Campos"
          />
        </div>
        <div
          class="grid grid-cols-1 sm:grid-cols-3 lg:grid-cols-3 gap-8 mt-12 xl:mt-0 xl:col-span-2 sm:justify-items-center mx-14 sm:mx-1"
        >
          <div
            class="flex-col md:grid md:grid-cols-1 md:gap-8"
            v-for="(i, index) in myList"
            :key="`title_${index}`"
          >
            <div class="flex flex-col">
              <h3 class="text-xl font-bold tracking-wider text-secondary">
                {{ i.title }}
              </h3>
              <ul role="list" class="mt-4 space-y-2 text-lg">
                <li
                  class=""
                  v-for="(subItem, sbIndex) in i.items"
                  :key="`item_${sbIndex}`"
                >
                  <div class="flex">
                    <NuxtLink
                      :to="subItem.href"
                      class="text-sm font-normal text-white hover:text-secondary flex-row"
                    >
                      <font-awesome-icon class="text-lg" :icon="subItem.icon" />
                      {{ subItem.label }}
                    </NuxtLink>
                  </div>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div
      class="px-5 py-5 mx-auto bg-gray-50 w-full sm:px-6 md:flex md:items-center md:justify-between lg:px-20"
    >
      <div class="flex justify-center mb-8 space-x-6 md:order-last md:mb-0">
        <AtomsButtonWhatsapp />
        <AtomsButtonInstagram />
        <AtomsButtonFacebook />
        <AtomsButtonLinkedin />
      </div>

      <div class="flex justify-center space-x-6 md:order-first md:mb-0">
        Todos os direitos reservados a Sabrina Campos
      </div>
    </div>
  </footer>
</template>
