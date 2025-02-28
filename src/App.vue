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
import DiapositiveMenu_IVA from './components/IVA/DiapositiveMenu_IVA.vue';

const diapositivaNumber = ref(1);
const maxDiapositiva = ref(1);
const title_pptx = ref('');
const currentPPTX = ref('');

const updateDiapositiva = (diapositiva) => {
  diapositivaNumber.value = diapositiva;
};

const updateMaxDiapositiva = (max) => {
  maxDiapositiva.value = max;
};

const updateTitle = (title) => {
  title_pptx.value = title;
};

const changePPTX = (pptx) => {
  currentPPTX.value = pptx;
};

const isDiapositiveMenuVisible = ref(true);
const hideDiapositiveMenu = () => {
  isDiapositiveMenuVisible.value = !isDiapositiveMenuVisible.value;
};

const isMenuLateraleVisible = ref(true);
const hideMenuLaterale = () => {
  isMenuLateraleVisible.value = !isMenuLateraleVisible.value;
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
    <TitleBar :title_pptx="title_pptx"/>
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
      <DiapositiveMenu_IVA v-if="isDiapositiveMenuVisible" @update-title="updateTitle" @update-diapositiva="updateDiapositiva" @update-max-diapositiva="updateMaxDiapositiva" />
      <div style="display:flex; align-items: center;">
      <Nascondi @click="hideDiapositiveMenu" :style="isDiapositiveMenuVisible ? '' : 'transform: rotate(180deg); margin-right: 121.26px'"/> <!-- width DiapositiveMenu 168.52px -->
      <DiapositivaCurrent_IlSistemaSolare style="max-height: 410px;" :diapositivaNumber="diapositivaNumber" />
      <Nascondi @click="hideMenuLaterale" :style="isMenuLateraleVisible && isDiapositiveMenuVisible ? 'transform: rotate(180deg)' : isMenuLateraleVisible && !isDiapositiveMenuVisible ? 'transform: rotate(180deg); margin-left: 84.26px' : (isDiapositiveMenuVisible ? 'margin-left: 37px' : 'margin-left: 121.26px')" /> <!-- width MenuLaterale 37px + width DiapositiveMenu 84.26px -->
      </div>
      <MenuLaterale v-if="isMenuLateraleVisible" />
    </div>
    <div class="footer">
      <p class="numberDiapositiva">Diapositiva {{diapositivaNumber}} di {{maxDiapositiva}}</p>
      <img src="./assets/Impress/footer.png" />
    </div>
  </div>

  <!-- Questi serviranno dopo per testare -->
  <br />
  <button>Il Sistema Solare.pptx</button>
  <button>SenzaNome1</button>
  <button>IVA.pptx</button>
  <button>Social Media Marketing.pptx</button>
  <!--  -->
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
  height: 410px;
}

.footer {
  display: flex;
  margin: none;
  align-items: center;
  height: 22px;
  border-top: 1px solid #c4c4c4;
}

.numberDiapositiva {
  margin: none;
  margin-left: 7px;
  font-size: 10px;
  margin-right: 4px;
  margin-bottom: 9px;
  width: 87px;
}
</style>