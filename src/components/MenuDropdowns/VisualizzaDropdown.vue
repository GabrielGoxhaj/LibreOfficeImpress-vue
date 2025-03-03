<template>
    <div id="dropdownVisualizza" class="dropdownVisualizza" :style="style">
      <a>Normale</a>
      <a>Struttura</a>
      <a>Note</a>
      <a>Ordine diapositive</a>
      <a>Diapositiva schema</a>
      <a>Note dello schema</a>
      <a>Stampato dello schema</a>
      <hr />
      <a>Interfaccia Utente</a>
      <a>Barre degli strumenti</a>
      <hr />
      <a>Barra di stato</a>
      <a>Pannello diapositive</a>
      <a>Barra a schede delle viste</a>
      <hr />
      <a>Righelli</a>
      <a>Griglia e linee guida</a>
      <a>Linee guida</a>
      <hr />
      <a>Commenti</a>
      <a>Colore/Toni di grigio</a>
      <hr />
      <a>Barra laterale</a>
      <a>Layout diapositiva</a>
      <a>Cambio diapositiva</a>
      <a>Animazione</a>
      <a>Stili</a>
      <a>Galleria</a>
      <a>Navigatore</a>
      <a>Barra dei colori</a>
      <a>Barra dei colori</a>
      <hr />
      <a>Sposta</a>
      <a>Zoom</a>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      style: {
        type: Object,
        default: () => ({})
      }
    }
  }
  </script>
  
  <style scoped>
  .dropdownVisualizza {
      position: absolute;
      background-color: #F2F2F2;
      width: 255px;
      height: auto;
      overflow: auto;
      box-shadow: 2px 2px 5px rgba(0, 0, 0, 0.2);
      border: lightgray;
      border-width: 1px;
      border-style: solid;
      z-index: 10;
  }
  
  .dropdownVisualizza a {
      color: black;
      text-decoration: none;
      font-family: 'Segoe UI', Tahoma, sans-serif;
      font-size: 9pt;
      display: block;
      margin-top: 1px;
      margin-left: 2px;
      padding-left: 7px;
      padding-top: 3px;
      padding-bottom: 3px;
      padding-right: 10px;
      transition: 0.1s;
      cursor: default;
  }
  
  .dropdownVisualizza a div {
      display: flex;
      align-items: center;
      padding: auto;
  }
  
  .dropdownVisualizza a div img {
      margin-right: 14px;
      max-width: 16px;
      max-height: 16px;
  }
  
  .dropdownVisualizza a:hover {
      background-color: #95cdfb;
  }
  
  hr {
      margin: 0;
      color: #d7d7d7;
  }
  </style>