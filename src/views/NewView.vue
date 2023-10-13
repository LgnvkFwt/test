<template>
  <main>
    <Input
      :model-value="classInput"
      @update:model-value="newValue => classInput = newValue"
    />
    <button @click="renderStr">GO</button>
    <div class="content">
        <BlockString 
            :templateString="templateString"
            @update:template-string="newValue => templateString = newValue"
        />
      <BlockDemo ref="test2" :templateComp="templateComp"/>
      <BlockDemoTemplate :template="templateComp"/>
    </div>
  </main>
</template>
<script setup>
import BlockDemo from '../components/BlockDemo.vue';
import BlockDemoTemplate from '../components/BlockDemo.template.vue';
import BlockString from '../components/BlockString.vue';
import { nextTick, ref, watch, unref } from 'vue';
import Input from '../components/InputClass.vue'


const aaa = `<div> 1231 {{ te }} </div>`;

const classInput = ref('');
const test2 = ref(null)
const templateString = ref('');
const templateComp = ref('');


function renderStr() {
        let template = templateString.value;
      const res = /\{\{(.*?)\}\}/g.exec(template);
      console.log(res[0])
      template = template.replace(new RegExp(res[0], 'gi'), classInput.value);
      templateComp.value = template;
}

// watch(classInput, () => {
//   nextTick().then(() => {
//     templateComp.value = test2.value.$el;
//     console.log( templateComp.value.attributes);
//     templateComp.value = templateComp.value.outerHTML;
//   })
// })
</script>

<style>
main {
height: 100%;
}
.content {
  display: flex;
  gap: 30px;
  padding: 30px 60px;
  height: 100%;
}
</style>
