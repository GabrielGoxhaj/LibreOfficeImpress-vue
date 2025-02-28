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
import DiapositiveMenu_IlSistemaSolare from './components/IlSistemaSolare/DiapositiveMenu_IlSistemaSolare.vue';
import MenuLaterale from './components/MenuLaterale.vue';
import Nascondi from './components/Nascondi.vue';
import DocumentiRecentiDropdown from './components/MenuDropdowns/FileDropdowns/DocumentiRecentiDropdown.vue';
import DiapositivaCurrent_IlSistemaSolare from './components/IlSistemaSolare/DiapositivaCurrent_IlSistemaSolare.vue';

const diapositivaNumber = ref(1);
const maxDiapositiva = ref(1);

const updateDiapositiva = (diapositiva) => {
  diapositivaNumber.value = diapositiva;
};

const updateMaxDiapositiva = (max) => {
  maxDiapositiva.value = max;
};

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
      <div id="dropdownsWrapper">
        <FileDropdown @toggle-dropdown="toggleDropdown" v-if="showDropdown === 'File'"
          :style="{ top: dropdownPosition.top + 'px', left: dropdownPosition.left + 'px' }" />
        <!-- <div id="dropdownsFileWrapper">
          <DocumentiRecentiDropdown v-if="showDropdown === 'DocumentiRecenti'"
            :style="{ top: dropdownPosition.top + 'px', left: dropdownPosition.left + 'px' }" />
        </div> -->
        <ModificaDropdown v-if="showDropdown === 'Modifica'"
          :style="{ top: dropdownPosition.top + 'px', left: dropdownPosition.left + 'px' }" />
        <VisualizzaDropdown v-if="showDropdown === 'Visualizza'"
          :style="{ top: dropdownPosition.top + 'px', left: dropdownPosition.left + 'px' }" />
        <InserisciDropdown v-if="showDropdown === 'Inserisci'"
          :style="{ top: dropdownPosition.top + 'px', left: dropdownPosition.left + 'px' }" />
        <FormatoDropdown v-if="showDropdown === 'Formato'"
          :style="{ top: dropdownPosition.top + 'px', left: dropdownPosition.left + 'px' }" />
        <DiapositivaDropdown v-if="showDropdown === 'Diapositiva'"
          :style="{ top: dropdownPosition.top + 'px', left: dropdownPosition.left + 'px' }" />
        <PresentazioneDropdown v-if="showDropdown === 'Presentazione'"
          :style="{ top: dropdownPosition.top + 'px', left: dropdownPosition.left + 'px' }" />
        <StrumentiDiapositiva v-if="showDropdown === 'Strumenti'"
          :style="{ top: dropdownPosition.top + 'px', left: dropdownPosition.left + 'px' }" />
        <FinestraDropdown v-if="showDropdown === 'Finestra'"
          :style="{ top: dropdownPosition.top + 'px', left: dropdownPosition.left + 'px' }" />
        <AiutoDropdown v-if="showDropdown === 'Aiuto'"
          :style="{ top: dropdownPosition.top + 'px', left: dropdownPosition.left + 'px' }" />
      </div>
      <MenuIconLibreOfficeImpress />
    </div>
    <div id="mainWrapper">
      <DiapositiveMenu_IlSistemaSolare @update-diapositiva="updateDiapositiva" @update-max-diapositiva="updateMaxDiapositiva" />
      <div style="display:flex; align-items: center;">
        <Nascondi />
        <DiapositivaCurrent_IlSistemaSolare :diapositivaNumber="diapositivaNumber" />
        <Nascondi style="transform: rotate(180deg);" />
      </div>
      <MenuLaterale />
    </div>
    <div style="display: flex; margin: none; align-items: center; height: 22px; border-top: 1px solid #c4c4c4;">
      <p style="margin: none; margin-left: 7px; font-size:12px; margin-right:4px;">Diapositiva {{diapositivaNumber}} di {{maxDiapositiva}}</p>
      <img src="./assets/Impress/footer.png" />
    </div>
  </div>
</template>

<style scoped>
.libreOfficeImpress {
  width: 800px;
  height: 560px;
  background-color: #f0f0f0;
  font-family: 'Segoe UI', Tahoma, sans-serif;
}

.menu {
  background-color: #fdfdfd;
  border-bottom: 1px solid #b0b0b0;
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

#mainWrapper {
  display: flex;
  flex-direction: row;
  width: 100%;
  justify-content: space-around;
}
</style>