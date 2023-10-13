<template>
    <div class="Block">
        <div class="Block__title">Block Demo Template</div>
        <textarea class="Block__template" :value="template" />
    </div>
    
</template>

<script setup>
defineProps(['template'])
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
    display: block;
    background-color: var(--background-sec);
    color: var(--text-color-sec);
    height: 100%;
    width: 100%;
    padding: 20px;
    word-wrap: break-word;
}
</style>