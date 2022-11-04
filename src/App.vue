<!-- <script setup>
import { onMounted, ref } from 'vue'
import webViewer from '@pdftron/webviewer'
import { propsToAttrMap } from '@vue/shared';


const viewer = ref();

onMounted(() => {
  // const path = `{process.env.BASE_URL}webviewer`
  const path = '/webviewer'
  // webViewer({path, initialDoc: 'https://filesamples.com/samples/document/docx/sample3.docx'}, viewer.value);
  // webViewer({path, initialDoc: '/images/rep.docx'}, viewer.value);   //docx
  // webViewer({path, initialDoc: 'https://cdn.hahu.jobs/public/aggregator/job-files/7da7ca29fa3d7c0316b9e23553f28be921bf448fc089c662b84c343047c2859cb915ca2ed55209f967191898e4644cf433ab'}, viewer.value);    //docx
  webViewer({path, initialDoc: 'https://cdn.hahu.jobs/public/aggregator/job-files/8e389c0b537464e2c0f6b45592b593a6388d1346b034049230ae39fba9e481ab635b57df591d6e972ca4394d5bf4f46acd9d'}, viewer.value);  //pdf


})

</script>
<template>
<div id="webviewer" ref="viewer">

</div>
</template>

<style>
#webviewer {
  height: 800px;
  width: 1000px;
}
</style> -->

<script setup>
import { ref } from 'vue'
import WebViewer from "./components/WebViewer.vue";
const link = ref(
  "https://cdn.hahu.jobs/public/aggregator/job-files/7da7ca29fa3d7c0316b9e23553f28be921bf448fc089c662b84c343047c2859cb915ca2ed55209f967191898e4644cf433ab"
);
</script>
<template>
  <div>
    <WebViewer :initialDoc="link" />
  </div>
</template>

