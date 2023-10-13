<template>
    <div class="Block">
        <div class="Block__title">Block Demo</div>
        <div class="Block__template" v-html="templateComp">
           
        </div>    
    </div>
    
</template>

<script setup>
import DynamicBlock from './DynamicBlock.vue'
defineProps(['templateComp'])
</script>

<style lang="css" scoped>
.Block {
    width: 100%;
    height: 100%;
}
.Block__title {
    font-size: 30px;
}
.Block__template {
    color: var(--text-color-sec);
    background-color: var(--background-sec);
    height: 100%;
    padding: 20px;
}
</style>