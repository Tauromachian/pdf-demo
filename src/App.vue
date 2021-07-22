<template>
  <div id="app">
    <vue-pdf-app style="height: 100vh;" :pdf="pdf" :config="config"></vue-pdf-app>
  </div>
</template>

<script>
// import { PDFJS } from "pdfjs-dist";
import VuePdfApp from "vue-pdf-app";
import getPdf from "./pdf";

export default {
  name: "App",

  data() {
    return {
      pdf: getPdf(),
      config: {
        toolbar: {
          toolbarViewerLeft: { findbar: false }
        }
      }
    };
  },
  components: {
    VuePdfApp,
  },
};
</script>

<style>
body {
  margin: 0;
}

.page {
  cursor: default;
  -webkit-user-select: none;  
  -moz-user-select: none;    
  -ms-user-select: none;      
  user-select: none;
}

.text-layer {
  cursor: default;

}

</style>
