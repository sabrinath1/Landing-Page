<script setup lang="ts">
import type { MenuOption } from "naive-ui";
import { RouterLink } from "vue-router";

const activeKey = ref(null);
const menuOptions = ref<MenuOption[]>([
  {
    label: () =>
      h(
        RouterLink,
        {
          to: {
            name: "",
          },
        },
        { default: () => "Home" }
      ),
    key: "home",
  },
  {
    label: () =>
      h(
        RouterLink,
        {
          to: {
            name: "",
          },
        },
        { default: () => "Sobre" }
      ),
    key: "about",
  },
  {
    label: () =>
      h(
        RouterLink,
        {
          to: {
            name: "",
          },
        },
        { default: () => "Serviços" }
      ),
    key: "services",
  },

  {
    label: () =>
      h(
        RouterLink,
        {
          to: {
            name: "",
          },
        },
        { default: () => "Contato" }
      ),
    key: "contact",
  },
]);
const social = useSocialRedirect();
</script>

<template>
  <div class="flex-none hidden lg:block justify-center items-center">
    <n-menu
      class="!font-semibold"
      v-model:value="activeKey"
      mode="horizontal"
      :options="menuOptions"
      :inverted="true"
    />
  </div>
</template>
