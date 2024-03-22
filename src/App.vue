<script setup>
import { ref } from 'vue'

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
    <p class="MsoNormal" style="margin-bottom: 8pt">
      <span style="font-size: 10pt; font-family: 'Arial', sans-serif; color: black">
        {{ firstName || firstNamePlaceholder }} {{ lastName || lastNamePlaceholder }}
      </span>
      <br />
      <span style="font-size: 8pt; font-family: 'Arial', sans-serif; color: #7f7f7f">
        {{ position || positionPlaceholder }}
      </span>
    </p>

    <p class="MsoNormal" style="margin-bottom: 8pt">
      <img width="115" height="68" src="./assets/logo.png" v:shapes="_x0000_i1025" /><br />

      <span
        style="font-size: 8pt; font-family: 'Arial', sans-serif; color: #ec733b; font-weight: bold"
      >
        ROCK YOUR LIFE! gGmbH
      </span>
      <br />
      <span
        style="font-size: 8pt; font-family: 'Arial', sans-serif; color: #7f7f7f; mso-no-proof: yes"
      >
        Developing potentials since 2008.
      </span>
    </p>

    <p class="MsoNormal" style="margin-bottom: 8pt">
      <span style="font-size: 8pt; font-family: 'Arial', sans-serif; color: #7f7f7f">
        Unsere Wirksamkeit ist wissenschaftlich bestätigt.
      </span>
      <span style="font-size: 8pt; font-family: 'Arial', sans-serif; color: #ec733b">
        <a
          href="https://rockyourlife.de/das-machen-wir/wirkung/"
          style="text-decoration: none; text-underline: none"
        >
          <span style="color: #ec733b">Mehr erfahren</span>
        </a>
      </span>
      <br />
      <span style="font-size: 8pt; font-family: 'Arial', sans-serif; color: #7f7f7f">
        Lust, uns zu unterstützen?&nbsp;
      </span>
      <span style="font-size: 8pt; font-family: 'Arial', sans-serif; color: #ec733b">
        <a
          href="https://rockyourlife.de/jetzt-spenden/?rock-your-life-ggmbh-3/spende"
          style="text-decoration: none; text-underline: none"
        >
          <span style="color: #ec733b">Hier</span>
        </a>
      </span>
      <span style="font-size: 8pt; font-family: 'Arial', sans-serif; color: #7f7f7f"
        >&nbsp;können Sie für uns spenden.</span
      >
    </p>

    <p class="MsoNormal" style="margin-bottom: 8pt">
      <span style="font-size: 8pt; font-family: 'Arial', sans-serif; color: #ec733b">Mail:</span
      ><span style="font-size: 8pt; font-family: 'Arial', sans-serif; color: #7f7f7f"
        >&nbsp;&nbsp;&nbsp;<a
          style="text-decoration: none; text-underline: none"
          :href="'mailto:' + email"
        >
          <span style="color: #7f7f7f">{{ email || emailPlaceholder }}</span></a
        ><br /> </span
      ><span style="font-size: 8pt; font-family: 'Arial', sans-serif; color: #ec733b"
        >Mobil&nbsp;&nbsp;</span
      ><span style="font-size: 8pt; font-family: 'Arial', sans-serif; color: #7f7f7f">{{
        phone || phonePlaceholder
      }}</span
      ><span style="font-size: 12pt; font-family: 'Times New Roman', serif; color: black"
        ><br /> </span
      ><span style="font-size: 8pt; font-family: 'Arial', sans-serif; color: #ec733b"
        >Web:&nbsp;&nbsp;</span
      ><span style="font-size: 8pt; font-family: 'Arial', sans-serif; color: #7f7f7f"
        ><a href="http://www.rockyourlife.de/" style="text-decoration: none; text-underline: none"
          ><span style="color: #7f7f7f; text-decoration: none; text-underline: none"
            >www.rockyourlife.de</span
          ></a
        >
      </span>
    </p>

    <p class="MsoNormal" style="margin-bottom: 8pt">
      <span style="font-size: 8pt; font-family: 'Arial', sans-serif; color: #7f7f7f"
        >Sitz der Gesellschaft:&nbsp;</span
      ><span style="font-size: 8pt; font-family: 'Arial', sans-serif; color: gray"
        >München; Amtsgericht München HRB 212 029<br />
        Geschäftsführung: Elisabeth Hahnke, Marvin Hiltrop, Stefan Schabernak</span
      >
    </p>
  </main>
</template>

<style scoped></style>
