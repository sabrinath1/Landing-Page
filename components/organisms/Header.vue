<script setup lang="ts">
const social = useSocialRedirect();
</script>
<template>
  <div
    class="w-full navbar bg-primary justify-between fixed z-50"
    id="header-top"
  >
    <div class="flex-none lg:hidden">
      <label for="my-drawer-3" class="btn btn-circle swap swap-rotate">
        <!-- hamburger icon -->
        <svg
          class="fill-current"
          xmlns="http://www.w3.org/2000/svg"
          width="32"
          height="32"
          viewBox="0 0 512 512"
        >
          <path
            d="M64,384H448V341.33H64Zm0-106.67H448V234.67H64ZM64,128v42.67H448V128Z"
          />
        </svg>
      </label>
    </div>
    <div class="flex px-2 mx-2 justify-end">
      <AtomsCompleteLogotipo></AtomsCompleteLogotipo>
    </div>
    <div class="flex-none hidden lg:block justify-center items-center">
      <MoleculesMenu></MoleculesMenu>
    </div>
    <div class="flex items-end space-x-4">
      <div class="hidden md:flex">
        <AtomsButtonContact @click="() => social.redirect('whatsapp')">
          Entrar em Contato</AtomsButtonContact
        >
      </div>
      <button
        class="hidden sm:flex"
        text
        style="font-size: 35px"
        @click="social.redirect('instagram')"
      >
        <Icon name="mdi:instagram" class="text-white transition-all" />
      </button>
      <button
        class="hidden sm:flex"
        text
        style="font-size: 35px"
        @click="social.redirect('linkedin')"
      >
        <Icon name="mdi:linkedin" class="text-white transition-all" />
      </button>
    </div>
    <div class="drawer-side">
      <label for="my-drawer-3" class="drawer-overlay"> </label>
    </div>
  </div>
</template>
