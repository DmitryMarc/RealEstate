<template>
    <div class="logo">
        <img 
            class="logo__img" 
            src="../assets/img/house-logo.png" 
            alt="logo" 
        />
        <a class="logo__title">
            Real estate
        </a>
    </div>
</template>

<style scoped lang="scss">
.logo{
    display: flex;
    justify-content: space-between;
    align-items: flex-end;
    gap: 10px;

    &__img{
        width: 40px;
    }

    &__title{
        font-weight: 500;
        font-size: 24px;
        color: #3C3C3B;
    }
}
</style>