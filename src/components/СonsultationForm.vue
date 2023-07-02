<template>
    <div class="consultation">
        <div class="consultation__advertisement">
            <h2 class="consultation__advertisement-title">
                Уютные квартиры со скидкой 10%
            </h2>
            <a class="consultation__advertisement-link">
                Узнать подробнее 
                <font-awesome-icon icon="angle-right" />
            </a>
            <div class="consultation__advertisement-pagination">
                <div>
                    <font-awesome-icon icon="angle-left" />
                    <span>1</span><span>/3</span>
                    <font-awesome-icon icon="angle-right" />
                </div>
            </div>
        </div>
        <div class="consultation__form">
            <div class="consultation__form-top">
                <h3 class="consultation__form-top-title">
                    Нужна консультация?
                </h3>
                <span class="consultation__form-top-description">
                    Оставьте заявку. Мы свяжемся с вами в течение 
                    <span>10 минут</span>
                </span>
            </div>
            <div class="consultation__form-content">
                <div class="consultation__form-content-item">
                    <label>Ваше имя</label>
                    <input placeholder="Ваше имя..." class="consultation__form-content-field" />
                </div>
                <div class="consultation__form-content-item">
                    <label>Email</label>
                    <input placeholder="Введите Email..." class="consultation__form-content-field" />
                </div>
                <div class="consultation__form-content-item">
                    <label>Номер телефона</label>
                    <input placeholder="+7 (XXX) XXX-XX-XX" class="consultation__form-content-field" />
                </div>
                <div class="consultation__form-content-item">
                    <label>Вопрос</label>
                    <input placeholder="Оставьте комментарий..." class="consultation__form-content-field" />
                </div>
            </div>
            <div class="consultation__form-bottom">
                <span class="consultation__form-bottom-confirmation">
                    Нажимая на кнопку Отправить, я подтверждаю согласие на 
                    <span>обработку персолнальных данных</span>
                </span>
                <!-- <button class="consultation__form-bottom-btn">
                    Отправить
                </button> -->
                <v-btn>
                    Отправить
                </v-btn>
            </div>
        </div>
    </div>
</template>

<script>
import VBtn from './UI/v-btn.vue';
export default {
    components:{
        VBtn
    }
}


</script>

<style scoped lang="scss">
.consultation{
    display: flex;
    justify-content: space-between;
    gap: 24px;

    &__advertisement{
        display: flex;
        flex-direction: column;
        gap: 32px;
        padding: 40px 32px;
        border-radius: 32px;
        background: 
            -70px bottom url('../assets/img/house-background.svg') no-repeat, 
            #719B2D;

        &-title{
            font-size: 48px;
            font-weight: 700;
            line-height: 56px;
            color: white;
            margin: 0;
        }

        &-link{
            display: flex;
            align-items: center;
            gap: 14px;
            font-size: 16px;
            font-weight: 500;
            color: white;
        }

        &-pagination{
            flex-grow: 1;
            display: flex;
            justify-content: flex-end;
            align-items: flex-end;

            color: white;
            opacity: .5;
        }
    }

    &__form{
        display: flex;
        flex-direction: column;
        gap: 70px;
        padding: 72px 70px;

        border-radius: 32px;
        background-color: #F6F6F6;

        &-content{
            width: 800px;
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;

            &-field{
                display: flex;
                flex-direction: column;
                width: 324px;
                padding: 18px 24px;
                border-radius: 32px;
                border: none;
            }
        }

        &-bottom{
            display: flex;
            gap: 50px;
            justify-content: space-between;

            &-confirmation{
                width: 372px;
                font-size: 14px;
            }

            &-btn{
                flex: 1;
                padding: 16px, 24px;

                font-size: 18px;
                font-weight: 500;
                color: white;

                border: none;
                border-radius: 32px;
                background-color: #719B2D;
                cursor: pointer;
            }
        }
    }
}
</style>