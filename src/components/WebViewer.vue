<template>
  <div id="webviewer" ref="viewer"></div>
</template>
<script setup>
import { ref, onMounted } from "vue";
import WebViewer from "@pdftron/webviewer";

const props = defineProps(["initialDoc"]);

const viewer = ref(null);
onMounted(() => {
  const path = "/webviewer";
  WebViewer({ path, initialDoc: props.initialDoc }, viewer.value);
});
</script>

<style>
#webviewer {
  height: 800px;
}
</style>
