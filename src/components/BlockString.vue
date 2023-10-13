<template>
    <div class="Block">
        <div class="Block__title">Block String</div>
        <textarea :value="templateString" @change="$emit('update:template-string', $event.target.value)" class="Block__template"></textarea>
    </div>
    
</template>

<script setup>
defineProps(['templateString'])
defineEmits(['update:template-string'])
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