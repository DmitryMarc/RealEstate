<template>
    <button class="btn">
        <slot>Кнопка</slot>
    </button>
</template>

<style scoped lang="scss">
.btn{
    display: flex;
    gap: 8px;
    align-items: baseline;
    padding: 8px 16px;

    font-size: 18px;
    font-weight: 500;
    color: #719B2D;

    border-radius: 24px;
    border: none;
    background-color: #F6F6F6;
    cursor: pointer;
}
</style>