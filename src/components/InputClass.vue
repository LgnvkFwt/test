<template>
    <div class="Input">
        <div class="Input__title">Введите класс</div>
        <input 
            class="Input__input"
            placeholder="Класс"
            :value="modelValue"
            @input="$emit('update:modelValue', $event.target.value)"
        />
    </div>
    
</template>

<script setup>
defineProps(['modelValue'])
defineEmits(['update:modelValue'])
</script>

<style scoped>
.Input {
    width: 340px;
    height: 70px;
    display: flex;
    flex-direction: column;
    margin: 0 60px;
}
.Input__title {
    color: var(--text-color);
    font-weight: 700;
    font-size: 12;
}

.Input__input {
    background-color: var(--background-sec);
    width: 100%;
    height: 100%;
    padding-left: 16px;
}
</style>