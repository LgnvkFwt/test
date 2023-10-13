<template>
    <div class="Dynamic" :class="classProp">
        <img src="https://adminlte.io/wp-content/uploads/2022/02/tailwindcss-templates.png" alt="123" class="Dynamic__image">
        <div class="Dynamic__content">
            <div class="Dynamic__title">Заголовок</div>
            <div class="Dynamic__template">
                Lorem ipsum dolor sit, amet consectetur adipisicing elit. Itaque sunt ab asperiores perferendis cum aut accusantium porro rerum possimus nemo delectus laborum quo alias reiciendis voluptas harum fuga, autem nobis!
            </div> 
        </div>
         
    </div>
    
</template>

<script setup>
defineProps(['classProp'])
</script>

<style lang="css" scoped>
.Dynamic {
    height: 400px;
    width: 400px;
    border: 1px solid var(--text-color-sec);
    display: flex;
    flex-direction: column;
}
.Dynamic__title {
    color: var(--text-color);
}
.Dynamic__content {
    padding: 0 20px;
}
.Dynamic__image {
    height: 50%;
    width: 100%;
}
</style>