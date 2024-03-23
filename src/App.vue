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
  <main>
    <div class="form">
      <label for="first-name">Vorname</label>
      <input type="text" id="first-name" :placeholder="firstNamePlaceholder" v-model="firstName" />
      <label for="last-name">Nachname</label>
      <input type="text" id="last-name" :placeholder="lastNamePlaceholder" v-model="lastName" />
      <label for="last-name">Position</label>
      <input type="text" id="last-name" :placeholder="positionPlaceholder" v-model="position" />
      <label for="email">E-Mail</label>
      <input type="text" id="email" :placeholder="emailPlaceholder" v-model="email" />
      <label for="phone">Telefonnummer (optional)</label>
      <span class="phoneHint">Die hier hinterlegte Nummer ist die vom Büro.</span>
      <input type="text" id="phone" :placeholder="phonePlaceholder" v-model="phone" />
    </div>

    <div class="emailWindow">
      <div class="menuBar">
        <span class="close"></span>
        <span class="minimize"></span>
        <span class="maximize"></span>
      </div>
      <div class="emailHeader">
        <div>An: Dein Empfänger</div>
        <div>Betreff: Meine neue E-Mail-Signatur</div>
      </div>

      <div class="emailBody">
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
      </div>
    </div>
  </main>
</template>

<style scoped>
main {
  display: flex;
  background: var(--gradient);
  min-height: 100vh;
  align-items: center;
}

.emailWindow {
  margin: auto;
}

.form {
  display: flex;
  flex-direction: column;
  flex-basis: 30%;
  background: white;
  padding: 40px;
  min-height: 100%;
  align-self: stretch;
  justify-content: center;
}

label {
  margin-bottom: 8px;
  color: var(--color-schoolgreen-80);
}

input {
  margin-bottom: 24px;
  height: 32px;
  border: 1px solid var(--color-iropink-100);
  border-radius: 4px;
  padding: 0 8px;
}

.menuBar {
  background: var(--color-schoolgreen-80);
  display: flex;
  align-items: center;
  height: 34px;
  border-bottom: 1px solid gray;
  border-radius: 8px 8px 0 0;
}

.close,
.minimize,
.maximize {
  display: block;
  width: 8px;
  height: 8px;
  border-radius: 100%;
  margin-right: 8px;
}

.close {
  background-color: rgb(224, 43, 61);
  margin-left: 16px;
}

.minimize {
  background-color: rgb(255, 188, 75);
}

.maximize {
  background-color: rgb(11, 143, 143);
}

.emailHeader {
  background: var(--color-schoolgreen-80);
  color: white;
  padding: 24px;
  line-height: 1.5;
}

.emailBody {
  background: white;
  padding: 60px 90px;
  border-radius: 0 0 8px 8px;
}

.phoneHint {
  font-size: 12px;
  color: var(--color-schoolgreen-80);
  margin-bottom: 8px;
}
</style>
