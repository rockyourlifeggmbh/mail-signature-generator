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

const defaultFontStyle = "font-size: 8pt; font-family: 'Arial', sans-serif; color: #7f7f7f;"
const linkStyle = 'text-decoration: none; text-underline: none;'
const highlightColor = 'color: #ec733b;'
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
    <p style="margin-bottom: 8pt">
      <span :style="defaultFontStyle + 'font-size: 10pt; color: black'">
        {{ firstName || firstNamePlaceholder }} {{ lastName || lastNamePlaceholder }}
      </span>
      <br />
      <span :style="defaultFontStyle">
        {{ position || positionPlaceholder }}
      </span>
    </p>

    <p style="margin-bottom: 8pt">
      <img width="115" src="./assets/logo.jpeg" style="margin: 4pt 0" />
      <br />
      <span :style="defaultFontStyle + highlightColor + 'font-weight: bold'">
        ROCK YOUR LIFE! gGmbH
      </span>
      <br />
      <span :style="defaultFontStyle">Developing potentials since 2008.</span>
    </p>

    <p style="margin-bottom: 8pt">
      <span :style="defaultFontStyle">Unsere Wirksamkeit ist wissenschaftlich bestätigt.</span>
      <a
        :style="defaultFontStyle + linkStyle + highlightColor"
        href="https://rockyourlife.de/das-machen-wir/wirkung/"
      >
        Mehr erfahren
      </a>
      <br />
      <span :style="defaultFontStyle">Lust, uns zu unterstützen?</span>
      <a
        :style="defaultFontStyle + linkStyle + highlightColor"
        href="https://rockyourlife.de/jetzt-spenden/?rock-your-life-ggmbh-3/spende"
      >
        Hier
      </a>
      <span :style="defaultFontStyle">können Sie für uns spenden.</span>
    </p>

    <p style="margin-bottom: 8pt">
      <span :style="defaultFontStyle + highlightColor">Mail:&nbsp;&nbsp;&nbsp;</span>
      <a :style="defaultFontStyle + linkStyle" :href="'mailto:' + email">
        {{ email || emailPlaceholder }}
      </a>
      <br />
      <span :style="defaultFontStyle + highlightColor">Mobil:&nbsp;&nbsp;</span>
      <span :style="defaultFontStyle">{{ phone || phonePlaceholder }}</span>
      <br />
      <span :style="defaultFontStyle + highlightColor">Web:&nbsp;&nbsp;</span>
      <a href="http://www.rockyourlife.de/" :style="defaultFontStyle + linkStyle">
        www.rockyourlife.de
      </a>
    </p>

    <p style="margin-bottom: 8pt">
      <span :style="defaultFontStyle">
        Sitz der Gesellschaft: München; Amtsgericht München HRB 212 029
      </span>
      <br />
      <span :style="defaultFontStyle">
        Geschäftsführung: Elisabeth Hahnke, Marvin Hiltrop, Stefan Schabernak
      </span>
    </p>
  </main>
</template>

<style scoped></style>
