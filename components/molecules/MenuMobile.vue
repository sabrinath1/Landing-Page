<script setup lang="ts">
const social = useSocialRedirect();
</script>

<template>
  <div
    class="menu p-4 w-80 bg-primary/80 backdrop-blur-sm text-base-content z-50"
  >
    <div class="flex justify-end">
      <label class="btn btn-circle swap swap-rotate">
        <!-- this hidden checkbox controls the state -->
        <input type="checkbox" />

        <!-- hamburger icon -->
        <svg
          class="swap-off fill-current"
          xmlns="http://www.w3.org/2000/svg"
          width="32"
          height="32"
          viewBox="0 0 512 512"
        >
          <path
            d="M64,384H448V341.33H64Zm0-106.67H448V234.67H64ZM64,128v42.67H448V128Z"
          />
        </svg>

        <!-- close icon -->
        <svg
          class="swap-on fill-current"
          xmlns="http://www.w3.org/2000/svg"
          width="32"
          height="32"
          viewBox="0 0 512 512"
        >
          <polygon
            points="400 145.49 366.51 112 256 222.51 145.49 112 112 145.49 222.51 256 112 366.51 145.49 400 256 289.49 366.51 400 400 366.51 289.49 256 400 145.49"
          />
        </svg>
      </label>
    </div>
    <MoleculesMenu />

    <div class="flex my-20 justify-center">
      <AtomsButtonContact></AtomsButtonContact>
    </div>
    <div class="flex justify-center mb-8 space-x-6 md:order-last md:mb-0">
      <n-button
        text
        style="font-size: 30px"
        @click="social.redirect('instagram')"
      >
        <Icon
          name="mdi:instagram"
          class="text-white hover:text-secondary transition-all"
        />
      </n-button>
      <n-button
        text
        style="font-size: 30px"
        @click="social.redirect('whatsapp')"
      >
        <Icon
          name="mdi:whatsapp"
          class="text-white hover:text-secondary transition-all"
        />
      </n-button>
      <n-button
        text
        style="font-size: 30px"
        @click="social.redirect('facebook')"
      >
        <Icon
          name="mdi:facebook"
          class="text-white hover:text-secondary transition-all"
        />
      </n-button>
      <n-button
        text
        style="font-size: 30px"
        @click="social.redirect('linkedin')"
      >
        <Icon
          name="mdi:linkedin"
          class="text-white hover:text-secondary transition-all"
        />
      </n-button>
    </div>
  </div>
</template>
