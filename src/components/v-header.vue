<template>
    <div class="header">
        <LogoEntity />
        <div class="header__links">
            <nav class="header__links-list">
                <a v-for="item in info" :key="item.id" href="#" class="active">
                    {{ item.linkTitle }}
                </a>
            </nav>
            <nav class="header__links-list">
                <a v-for="item in filters" :key="item.id" href="#">
                    {{ item.linkTitle }}
                </a>
            </nav>
        </div>
        <div class="header__contacts">
            <v-extra-btn>
                <font-awesome-icon icon="location-dot" />
                Санкт-Петербург
            </v-extra-btn>
            <span class="header__contacts-number">
                +7 (812) 910 00 60
            </span>
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
            info:[
                {
                    id: '0',
                    linkTitle: 'О компании'
                },
                {
                    id: '1',
                    linkTitle: 'Инвесторам'
                },
                {
                    id: '2',
                    linkTitle: 'Для жителей'
                }
            ],
            filters: [
                {
                    id: '0',
                    linkTitle: 'Новостройки'
                },
                {
                    id: '1',
                    linkTitle: 'Вторички'
                },
                {
                    id: '2',
                    linkTitle: 'Комерческая'
                },
                {
                    id: '3',
                    linkTitle: 'Загородная'
                },
                {
                    id: '4',
                    linkTitle: 'Аренда'
                },
                {
                    id: '5',
                    linkTitle: 'Ипотека'
                }
            ]
        }
    }
}

</script>


<style scoped lang="scss">

.header{
    display: flex;
    justify-content: space-between;
    
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

    a.active{
        color: #587725
    }

    &__contacts{
        display: flex;
        align-items: flex-end;
        gap: 16px;

        &-number{
            font-size: 24px;
            font-weight: 500;
        }
    }
}

</style>