<template lang="pug">
  #app
    LogUploader
</template>

<script lang="ts">
  import {Component, Vue} from "vue-property-decorator";
  import LogUploader from "./components/LogUploader.vue";

  @Component({
    components: {
      LogUploader,
    },
  })
  export default class App extends Vue {
  }
</script>

<style>
  :root {
    --font-roboto: 'Roboto', sans-serif;
  }

  #app {
    font-family: var(--font-roboto);
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
  }
</style>
