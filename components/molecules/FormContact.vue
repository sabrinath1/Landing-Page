<script setup lang="ts">
import { FormKit } from "@formkit/vue";

const myInput = ref();

const showModal = ref(true);

showModal.value = true;

myInput?.value?.node?.reset();
</script>
<template>
  <div class="bg-secondary text-white py-10">
    <FormKit
      ref="myInput"
      type="form"
      name="formContact
      "
      submit-label="Enviar Mensagem"
      :submit-attrs="{
        inputClass: '!bg-secondary',
      }"
    >
      <div>
        <FormKit
          label="Nome"
          type="text"
          name="name"
          label-class="text-white"
          placeholder="Nome Completo"
          validation="required"
        />
      </div>
      <div>
        <FormKit
          type="tel"
          label-class="text-white"
          label="Celular"
          placeholder="(__)_____-____"
          mask="(99)99999-9999"
          :validation="[
            ['required'],
            ['matches', /^[0-9]{2}[0-9]{5}[0-9]{4}$/],
          ]"
          name="phone"
          :validation-messages="{
            matches: 'Numero de celular com discagem incorreta',
          }"
          validation-visibility="dirty"
          max="11"
        />
      </div>
      <div>
        <FormKit
          type="email"
          label-class="text-white"
          label="E-mail"
          validation-visibility="live"
          placeholder="email@email.com"
          name="email"
          validation="required|email"
          :validation-messages="{
            email: 'E-mail com formato incorreto',
          }"
        />
      </div>
      <FormKit
        type="textarea"
        label-class="text-white"
        label="Mensagem"
        name="message"
        placeholder="Digite sua mensagem ..."
        rows="10"
        maxlength="500"
        validation="required"
      />
    </FormKit>
    <!-- <n-modal
      class="max-w-md"
      v-model:show="showModal"
      preset="card"
      title=" Obrigado por entrar em contato conosco!"
    >
      <div class="text-secondary">
        <br />Recebemos sua mensagem e entraremos em contato o mais breve
        possível para discutir sua situação. <br />Seu caso é importante para
        nós, e faremos o possível para fornecer a assistência jurídica
        necessária para ajudá-lo a resolver seus problemas legais.
      </div>
    </n-modal> -->
  </div>
</template>
