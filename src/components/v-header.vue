<template>
    <div class="header">
        <div class="header__logo">
            <img class="header__logo-img" src="../assets/img/house-logo.png" alt="logo" />
            <a class="header__logo-title">
                Real estate
            </a>
        </div>
        <div class="header__links">
            <nav class="header__links-list">
                <a href="#">О компании</a>
                <a href="#">Инвесторам</a>
                <a href="#">Для жителей</a>
            </nav>
            <nav class="header__links-list">
                <a href="#">Новостройки</a>
                <a href="#">Вторички</a>
                <a href="#">Комерческая</a>
                <a href="#">Загородная</a>
                <a href="#">Аренда</a>
                <a href="#">Ипотека</a>
            </nav>
        </div>
        <div class="header__contacts">
            <button class="header__contacts-location">
                <font-awesome-icon icon="location-dot" />
                Санкт-Петербург
            </button>
            <span class="header__contacts-number">
                +7 (812) 910 00 60
            </span>
        </div>
    </div>
</template>


<style scoped lang="scss">

.header{
    display: flex;
    justify-content: space-between;

    &__logo{
        display: flex;
        justify-content: space-between;
        align-items: flex-end;
        gap: 10px;

        &-img{
            width: 40px;
        }

        &-title{
            font-weight: 500;
            font-size: 24px;
            color: #3C3C3B;
        }
    }
    
    &__links{
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        row-gap: 10px;

        &-list{
            display: flex;
            column-gap: 24px;

            &:first-child{
                font-size: 16px;
                
                a{
                    color: #9A9A9A;
                }
            }

            &:last-child{
                font-size: 18px;
                
                a{
                    color: #3C3C3B;
                }
            }
        }
    }

    &__contacts{
        display: flex;
        align-items: flex-end;
        gap: 16px;

        &-location{
            display: flex;
            gap: 8px;
            align-items: center;
            padding: 8px 16px;

            font-size: 18px;
            font-weight: 500;
            color: #719B2D;

            border-radius: 24px;
            border: none;
            background-color: #F6F6F6;
            cursor: pointer;
        }

        &-number{
            font-size: 24px;
            font-weight: 500;
        }
    }
}

</style>