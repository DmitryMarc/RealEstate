<template>
    <button class="btn">
        <slot>Кнопка</slot>
    </button>
</template>

<style scoped lang="scss">
.btn{
    flex: 1;
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 16px;
    padding: 16px 24px;

    font-size: 18px;
    font-weight: 500;
    color: white;

    border: none;
    border-radius: 32px;
    background-color: #719B2D;
    cursor: pointer;
}

</style>