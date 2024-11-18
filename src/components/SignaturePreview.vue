<script setup>
defineProps({
  firstName: String,
  firstNamePlaceholder: String,
  lastName: String,
  lastNamePlaceholder: String,
  position: String,
  positionPlaceholder: String,
  email: String,
  emailPlaceholder: String,
  phone: String,
  phonePlaceholder: String
})

const defaultFontStyle = "font-size: 8pt; font-family: 'Arial', sans-serif; color: #7f7f7f;"
const linkStyle = 'text-decoration: none; text-underline: none;'
const highlightColor = 'color: #ec733b;'
const marginBottom = 'margin-bottom: 8pt;'
</script>

<template>
  <div>
    <p :style="marginBottom">
      <span :style="defaultFontStyle + 'font-size: 10pt; color: black'">
        {{ firstName || firstNamePlaceholder }} {{ lastName || lastNamePlaceholder }}
      </span>
      <br />
      <span :style="defaultFontStyle">
        {{ position || positionPlaceholder }}
      </span>
    </p>

    <p :style="marginBottom">
      <img width="115" src="../assets/logo.jpeg" style="margin: 4pt 0" />
      <br />
      <span :style="defaultFontStyle + highlightColor + 'font-weight: bold'">
        ROCK YOUR LIFE! gGmbH
      </span>
      <br />
      <span :style="defaultFontStyle">Developing potentials since 2008.</span>
    </p>

    <p :style="marginBottom">
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

    <p :style="marginBottom">
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

    <p :style="marginBottom">
      <span :style="defaultFontStyle">
        Sitz der Gesellschaft: München; Amtsgericht München HRB 212 029
      </span>
      <br />
      <span :style="defaultFontStyle"> Geschäftsführung: Marvin Hiltrop, Stefan Schabernak </span>
    </p>
  </div>
</template>
