<template lang="pug">
  div(:class="uploadAreaClassList")
    .upload-area__text {{uploadAreaText}}
</template>

<script lang="ts">
  import {Component, Prop, Vue} from "vue-property-decorator";


  @Component({
    components: {},
  })
  export default class LogUploader extends Vue {
    private uploadAreaText: string = "Please, drag a log file here.";
    private uploadAreaClassList: { [className: string]: boolean } = {
      "upload-area": true,
      "upload-area_drag": false,
    };

    private mounted() {
      document.addEventListener("dragenter", this.onDragEnter, false);
    }

    private onDragEnter(ev: DragEvent) {
      console.error(d);
    }

    private beforeUnmount() {
      document.removeEventListener("dragenter", this.onDragEnter, false);
    }
  }
</script>

<style>
  .upload-area {
    padding: 1rem;
    width: 12rem;
    height: 8rem;
    border: 1px dashed #cdcdcd;
    position: relative;
    transition: background-color 0.4s ease;
  }
</style>
