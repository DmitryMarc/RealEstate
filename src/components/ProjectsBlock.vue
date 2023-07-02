<template>
    <div class="projects">
        <h2 class="projects__title">
            Наши <span>проекты</span>
        </h2>
        <div class="projects__filters">
            <div class="projects__filters-item">
                <label class="projects__filters-title">
                    Выберите локацию
                </label>
                <div class="projects__filters-location">
                    <span>Район</span>
                    <font-awesome-icon icon="angle-down" />
                </div>
            </div>

            <div class="projects__filters-item">
                <label class="projects__filters-title">
                    Задайте стоимость
                </label>
                <div class="projects__filters-price">
                    <span>от 2,9</span>
                    <span>—</span>
                    <span>до 19,2</span>
                </div>
            </div>
            <div class="projects__filters-item">
                <!-- <button>Только со скидкой</button> -->
                <v-btn>
                    Только со скидкой
                    <font-awesome-icon icon="circle-dot" />
                </v-btn>
                <button class="projects__filters-reset">
                    <label class="projects__filters-title">Сбросить все фильтры</label>
                    <font-awesome-icon icon="xmark" />
                </button>
            </div>

        </div>
        <CaldsList />
    </div>
</template>

<script>
import VBtn from './UI/v-btn.vue';
import CaldsList from './CardsList.vue';


export default {
    components: {
        VBtn,
        CaldsList
    }
}

</script>

<style scoped lang="scss">
.projects{
    display: flex;
    flex-direction: column;
    gap: 50px;

    &__title{
        margin: 0;
        font-size: 40px;
        font-weight: 700;
        color: #3C3C3B;
    }

    &__filters{
        display: flex;
        justify-content: space-between;
        align-items: flex-end;
        gap: 24px;

        &-item{
            display: flex;
            flex: 1;
            gap: 16px;

            &:not(:last-child){
                flex-direction: column;
                font-size: 18px;
                font-weight: 500;
            }
        }

        &-title{
            font-size: 12px;
            font-weight: 500;
            color: #9A9A9A;
        }

        &-location,
        &-price{
            display: flex;
            justify-content: space-between;
            align-items: center;
            background-color: #F6F6F6;
            border-radius: 32px;
            padding: 18px 24px;
        }

        &-reset{
            display: flex;
            align-items: center;
            gap: 8px;
            border: none;
            background-color: white;
        }

    }
}
</style>