<template>
  <div class="drawer">
    <input id="my-drawer-3" type="checkbox" class="drawer-toggle" />
    <div class="drawer-content flex flex-col">
      <!-- Navbar -->
      <OrganismsHeader />

      <div class="mb-20 mt-20">
        <slot></slot>
      </div>
      <OrganismsRodape
        title="Sabrina Campos Advocacia"
        about="Somos um escritório de advocacia comprometido em fornecer serviços jurídicos de excelência, com foco nas necessidades e objetivos de nossos clientes. Com anos de experiência, nossa equipe de advogados altamente qualificados está pronta para oferecer soluções jurídicas eficazes e personalizadas."
      />
    </div>
    <div class="drawer-side">
      <label for="my-drawer-3" class="drawer-overlay"> </label>
    </div>
  </div>
</template>
