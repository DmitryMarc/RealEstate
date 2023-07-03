<template>
    <div class="footer">
        <div class="footer__info">
            <LogoEntity />
            <div class="footer__info-contacts">
                <v-extra-btn>
                    <font-awesome-icon icon="location-dot" />
                    Санкт-Петербург
                </v-extra-btn>
                <span class="footer__info-number">
                    +7 (812) 910 00 60
                </span>
            </div>
            <span class="footer__info-confirmation">
                База данных о недвижимости. Использование сайта 
                означает согласие с 
                <span class="footer__mark">Пользовательским соглашением</span> и 
                <span class="footer__mark">Политикой конфиденциальности</span>. 
                Оплачивая лицензионный 
                платеж, вы принимаете Лицензионное соглашение
            </span>
        </div>
        <div 
            class="footer__navigation" 
            v-for="item in linksList" 
            :key="item.title"
        >
            <div class="footer__navigation-col">
                <h4 class="footer__navigation-title">
                    Проекты
                </h4>
                <nav class="footer__navigation-links">
                    <a v-for="link in item.links" :key="link.id" href="#">
                        {{ link.title }}
                    </a>
                </nav>
            </div>
        </div>
    </div>
</template>

<script>
import LogoEntity from './LogoEntity.vue';
import VExtraBtn from './UI/v-extra-btn.vue'

export default {
    components:{
        LogoEntity,
        VExtraBtn
    },
    data(){
        return {
            linksList: [
                {   
                    title: 'Проекты',
                    links: [
                        {
                            id: '0',
                            title: 'Название проекта'
                        },
                        {
                            id: '1',
                            title: 'Название проекта'
                        },
                        {
                            id: '2',
                            title: 'Название проекта'
                        },
                        {
                            id: '3',
                            title: 'Название проекта'
                        },
                        {
                            id: '4',
                            title: 'Название проекта'
                        },
                        {
                            id: '5',
                            title: 'Название проекта'
                        }
                    ],
                },
                {   
                    title: 'О компании',
                    links: [
                        {
                            id: '0',
                            title: 'Новости'
                        },
                        {
                            id: '1',
                            title: 'Пресс-релизы'
                        },
                        {
                            id: '2',
                            title: 'Логотип'
                        },
                        {
                            id: '3',
                            title: 'Инвесторам'
                        },
                        {
                            id: '4',
                            title: 'Карьера'
                        },
                        {
                            id: '5',
                            title: 'Застройщикам'
                        }
                    ],
                },
                {   
                    title: 'Наши предложения',
                    links: [
                        {
                            id: '0',
                            title: 'Новостройки'
                        },
                        {
                            id: '1',
                            title: 'Вторички'
                        },
                        {
                            id: '2',
                            title: 'Комерческая'
                        },
                        {
                            id: '3',
                            title: 'Загородная'
                        },
                        {
                            id: '4',
                            title: 'Аренда'
                        },
                        {
                            id: '5',
                            title: 'Ипотека'
                        }
                    ],
                }
            ]
        }
    }
}
</script>

<style scoped lang="scss">
.footer{
    display: flex;
    justify-content: space-between;
    gap: 90px;

    padding: 54px 0;

    &__info{
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: flex-start;
        gap: 34px;

        max-width: 420px;

        &-contacts{
            display: flex;
            justify-content: space-between;
            gap: 24px;
        }

        &-number{
            display: flex;
            align-items: center;
            font-size: 18px;
            font-weight: 500;
            color: #3C3C3B;
        }

        &-confirmation{
            font-size: 12px;
            font-weight: 400;
            color: #9A9A9A
        }
    }

    &__navigation{
        display: flex;
        justify-content: space-between;
        gap: 120px;

        &-col{
            display: flex;
            flex-direction: column;
            gap: 24px;
        }

        &-title{
            margin: 0;
            text-transform: uppercase;

            font-size: 12px;
            font-weight: 500;
            color: #9A9A9A;
        }
        
        &-links{
            display: flex;
            flex-direction: column;
            gap: 10px;

            a{
                font-size: 16px;
                font-weight: 500;
                color: #3C3C3B;
            }
        }
    }

    &__mark{
        color:#719B2D
    }
}

</style>