<script setup lang="ts">
const myList = ref([
  {
    title: "Sobre",
    items: [
      {
        label: "Quem Somos",
        href: "#",
        icon: "",
      },
      {
        label: "Serviços",
        href: "#",
        icon: "",
      },
      {
        label: "Contato",
        href: "#",
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
        icon: "fa-mobile-screen",
      },
      {
        label: "sabrina@advocacia.com.br",
        href: "",
        icon: "fa-envelope",
      },
      {
        label: "Av. Dr. Afonso Vergueiro, 5000- Centro, Sorocaba - SP",
        href: "",
        icon: "fa-map-location-dot",
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
        icon: "fa-clock",
      },
    ],
  },
]);
const props = defineProps<{
  about: string;
  title: string;
}>();
const social = useSocialRedirect();
</script>

<template>
  <footer class="bg-primary" aria-labelledby="footer-heading ">
    <div class="px-4 py-12 mx-auto w-full sm:px-6 lg:px-16">
      <div class="xl:grid xl:grid-cols-3 xl:gap-8">
        <div class="flex flex-col justify-center items-center my-3">
          <a
            class="text-3xl md:text-4xl font-bold tracking-tighter text-secondary transition duration-500 ease-in-out transform tracking-relaxed lg:pr-8"
          >
            {{ props.title }}
          </a>
          <p
            class="md:w-1/2 xl:w-auto mt-2 sm:mt-7 text-sm text-base-100 mx-5 text-center w-full"
          >
            {{ props.about }}
          </p>
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
              <h3 class="text-xl font-bold tracking-wider text-white">
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
        <n-button
          text
          style="font-size: 30px"
          @click="social.redirect('instagram')"
        >
          <Icon
            name="mdi:instagram"
            class="text-primary hover:text-secondary transition-all"
          />
        </n-button>
        <n-button
          text
          style="font-size: 30px"
          @click="social.redirect('whatsapp')"
        >
          <Icon
            name="mdi:whatsapp"
            class="text-primary hover:text-secondary transition-all"
          />
        </n-button>
        <n-button
          text
          style="font-size: 30px"
          @click="social.redirect('facebook')"
        >
          <Icon
            name="mdi:facebook"
            class="text-primary hover:text-secondary transition-all"
          />
        </n-button>
        <n-button
          text
          style="font-size: 30px"
          @click="social.redirect('linkedin')"
        >
          <Icon
            name="mdi:linkedin"
            class="text-primary hover:text-secondary transition-all"
          />
        </n-button>
      </div>

      <div class="mt-8 md:mt-0 md:order-1 justify-items-center">
        <span class="mt-2 text-sm font-light text-primary">
          Todos os direitos reservados a Sabrina Campos
          <a
            href="https://wickedlabs.dev"
            class="mx-2 text-wickedblue hover:text-secondary"
            rel="noopener noreferrer"
          ></a>
        </span>
      </div>
    </div>
  </footer>
</template>
