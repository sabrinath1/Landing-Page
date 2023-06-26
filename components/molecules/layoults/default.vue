<script setup lang="ts">
import { NThemeEditor } from "naive-ui";
</script>
<template>
  <div class="drawer">
    <input id="my-drawer-3" type="checkbox" class="drawer-toggle" />
    <div class="drawer-content flex flex-col">
      <!-- Navbar -->
      <OrganismsHeader />
      <slot></slot>
      <div class="mb-20"></div>
      <OrganismsRodape
        title="Vizzon Advocacia"
        about=" O escritório nasceu da vontade de acolher as necessidades das pessoas que enfrentam conflitos familiares, pessoais e empresariais."
      />
    </div>
    <div class="drawer-side">
      <label for="my-drawer-3" class="drawer-overlay"> </label>
      <MoleculesMenuMobile />
    </div>
  </div>
</template>
