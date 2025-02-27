<script setup>
import { ref } from 'vue';
import MenuLibreOfficeImpress from './components/MenuLibreOfficeImpress.vue';
import MenuIconLibreOfficeImpress from './components/MenuIconLibreOfficeImpress.vue';
import TitleBar from './components/TitleBar.vue';
import FileDropdown from './components/MenuDropdowns/FileDropdown.vue';
import ModificaDropdown from './components/MenuDropdowns/ModificaDropdown.vue';
import VisualizzaDropdown from './components/MenuDropdowns/VisualizzaDropdown.vue';
import InserisciDropdown from './components/MenuDropdowns/InserisciDropdown.vue';
import FormatoDropdown from './components/MenuDropdowns/FormatoDropdown.vue';
import DiapositivaDropdown from './components/MenuDropdowns/DiapositivaDropdown.vue';
import PresentazioneDropdown from './components/MenuDropdowns/PresentazioneDropdown.vue';
import StrumentiDiapositiva from './components/MenuDropdowns/StrumentiDiapositiva.vue';
import FinestraDropdown from './components/MenuDropdowns/FinestraDropdown.vue';
import AiutoDropdown from './components/MenuDropdowns/AiutoDropdown.vue';

const showDropdown = ref(null);
const dropdownPosition = ref({ top: 0, left: 0 });

const toggleDropdown = ({ type, position }) => {
  showDropdown.value = showDropdown.value === type ? null : type;
  dropdownPosition.value = position;
};
</script>

<template>
  <div class="libreOfficeImpress">
    <TitleBar />
    <div class="menu">
      <MenuLibreOfficeImpress @toggle-dropdown="toggleDropdown" />
      <MenuIconLibreOfficeImpress />
    </div>
    <FileDropdown v-if="showDropdown === 'File'" :style="{ top: dropdownPosition.top + 'px', left: dropdownPosition.left + 'px' }" />
    <ModificaDropdown v-if="showDropdown === 'Modifica'" :style="{ top: dropdownPosition.top + 'px', left: dropdownPosition.left + 'px' }" />
    <VisualizzaDropdown v-if="showDropdown === 'Visualizza'" :style="{ top: dropdownPosition.top + 'px', left: dropdownPosition.left + 'px' }" />
    <InserisciDropdown v-if="showDropdown === 'Inserisci'" :style="{ top: dropdownPosition.top + 'px', left: dropdownPosition.left + 'px' }" />
    <FormatoDropdown v-if="showDropdown === 'Formato'" :style="{ top: dropdownPosition.top + 'px', left: dropdownPosition.left + 'px' }" />
    <DiapositivaDropdown v-if="showDropdown === 'Diapositiva'" :style="{ top: dropdownPosition.top + 'px', left: dropdownPosition.left + 'px' }" />
    <PresentazioneDropdown v-if="showDropdown === 'Presentazione'" :style="{ top: dropdownPosition.top + 'px', left: dropdownPosition.left + 'px' }" />
    <StrumentiDiapositiva v-if="showDropdown === 'Strumenti'" :style="{ top: dropdownPosition.top + 'px', left: dropdownPosition.left + 'px' }" />
    <FinestraDropdown v-if="showDropdown === 'Finestra'" :style="{ top: dropdownPosition.top + 'px', left: dropdownPosition.left + 'px' }" />
    <AiutoDropdown v-if="showDropdown === 'Aiuto'" :style="{ top: dropdownPosition.top + 'px', left: dropdownPosition.left + 'px' }" />
  </div>
</template>

<style scoped>
.libreOfficeImpress {
  width: 800px;
  height: 560px;
  background-color: #f0f0f0;
}

.menu {
  background-color: #fdfdfd;
}

.libreOfficeImpress {
  border: 1px solid black;
}

hr {
  display: block;
  margin-left: auto;
  margin-right: auto;
  margin-top: 0;
  margin-bottom: 0;
}
</style>