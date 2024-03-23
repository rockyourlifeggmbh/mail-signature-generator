<script setup>
import { ref } from 'vue'
import SignaturePreview from './components/SignaturePreview.vue'

const firstName = ref('')
const firstNamePlaceholder = 'Stafan'

const lastName = ref('')
const lastNamePlaceholder = 'Schabernak'

const position = ref('')
const positionPlaceholder = 'Geschäftsführer'

const email = ref('')
const emailPlaceholder = 'stefan.schabernak@rockyourlife.de'

const phone = ref('')
const phonePlaceholder = '+49 (0) 89 / 224 106 22'
</script>

<template>
  <header>
    <label for="first-name">Vorname</label>
    <input type="text" id="first-name" :placeholder="firstNamePlaceholder" v-model="firstName" />
    <label for="last-name">Nachname</label>
    <input type="text" id="last-name" :placeholder="lastNamePlaceholder" v-model="lastName" />
    <label for="last-name">Position</label>
    <input type="text" id="last-name" :placeholder="positionPlaceholder" v-model="position" />
    <label for="email">E-Mail</label>
    <input type="text" id="email" :placeholder="emailPlaceholder" v-model="email" />
    <label for="phone">Telefonnummer</label>
    <input type="text" id="phone" :placeholder="phonePlaceholder" v-model="phone" />
  </header>

  <main>
    <SignaturePreview
      :first-name="firstName"
      :first-name-placeholder="firstNamePlaceholder"
      :last-name="lastName"
      :last-name-placeholder="lastNamePlaceholder"
      :position="position"
      :position-placeholder="positionPlaceholder"
      :email="email"
      :email-placeholder="emailPlaceholder"
      :phone="phone"
      :phone-placeholder="phonePlaceholder"
    />
  </main>
</template>

<style scoped></style>
