<template>
    <div class="consultation">
        <swiper
            :modules="modules" 
            :slides-per-view="1" 
            :navigation="{
                prevEl: '#swiper-prev',
                nextEl: '#swiper-next'
            }" 
        >
            <swiper-slide
                v-for="item in 3"
                :key="item"
            >
                <div class="consultation__advertisement">
                    <h2 class="consultation__advertisement-title">
                        Уютные квартиры со скидкой 10%
                    </h2>
                    <a class="consultation__advertisement-link">
                        Узнать подробнее
                        <font-awesome-icon icon="angle-right" />
                    </a>
                </div>
            </swiper-slide>
        </swiper>
        <div class="consultation__advertisement-pagination">
            <font-awesome-icon icon="angle-left" :id="'swiper-prev'" @click="changeSlideHandler('prev')" />
            <span>{{ currentPage }}</span><span>/ {{ totalPages }}</span>
            <font-awesome-icon icon="angle-right" :id="'swiper-next'" @click="changeSlideHandler('next')" />
        </div>
        <div class="consultation__form">
            <div class="consultation__form-top">
                <h3 class="consultation__form-top-title">
                    Нужна консультация?
                </h3>
                <span class="consultation__form-top-description">
                    Оставьте заявку. Мы свяжемся с вами в течение
                    <span class="consultation__mark">10 минут</span>
                </span>
            </div>

            <div class="consultation__form-content">
                <div class="consultation__form-content-item">
                    <label class="consultation__form-content-title">
                        <img src="../assets/img/icons/user-icon.svg" />
                        Ваше имя
                    </label>
                    <input placeholder="Ваше имя..." class="consultation__form-content-field" />
                </div>
                <div class="consultation__form-content-item">
                    <label class="consultation__form-content-title">
                        <img src="../assets/img/icons/email-icon.svg" />
                        Email
                    </label>
                    <input placeholder="Введите Email..." class="consultation__form-content-field" />
                </div>
                <div class="consultation__form-content-item">
                    <label class="consultation__form-content-title">
                        <img src="../assets/img/icons/call-icon.svg" />
                        Номер телефона
                    </label>
                    <input placeholder="+7 (XXX) XXX-XX-XX" class="consultation__form-content-field" />
                </div>
                <div class="consultation__form-content-item">
                    <label class="consultation__form-content-title">
                        <img src="../assets/img/icons/question-icon.svg" />
                        Вопрос
                    </label>
                    <input placeholder="Оставьте комментарий..." class="consultation__form-content-field" />
                </div>
            </div>

            <div class="consultation__form-bottom">
                <span class="consultation__form-bottom-confirmation">
                    Нажимая на кнопку Отправить, я подтверждаю согласие на
                    <span class="consultation__mark">
                        обработку персолнальных данных

                    </span>
                </span>

                <v-basic-btn>
                    Отправить
                </v-basic-btn>
            </div>
        </div>
    </div>
</template>

<script>
import { Navigation } from 'swiper/modules';
import { Swiper, SwiperSlide } from 'swiper/vue';

import 'swiper/css';
import 'swiper/css/navigation';
import 'swiper/css/pagination';

import VBasicBtn from './UI/v-basic-btn.vue';
export default {
    components: {
        VBasicBtn,
        Swiper,
        SwiperSlide
    },
    setup() {
        const onSwiper = (swiper) => {
            console.log(swiper);
        };
        const onSlideChange = () => {
            console.log('slide change');
        };
        return {
            onSwiper,
            onSlideChange,
            modules: [Navigation],
        };
    },
    data(){
        return{
            currentPage: 1,
            totalPages: 3
        }
    },
    methods:{
        changeSlideHandler(value){
            switch (value) {
                case 'prev': {
                    if (this.currentPage > 1) this.currentPage--;
                    break;
                }
                case 'next':{
                    if (this.currentPage < this.totalPages) this.currentPage++;
                    break;
                }
            }
        }
    }
}

</script>

<style scoped lang="scss">
.consultation {
    display: flex;
    justify-content: space-between;
    gap: 24px;
    position: relative;

    &__advertisement {
        height: 100%;
        display: flex;
        flex-direction: column;
        gap: 32px;
        padding: 40px 32px;
        border-radius: 32px;
        background:
            -70px bottom url('../assets/img/house-background.svg') no-repeat,
            #719B2D;
        box-sizing: border-box;
            
        &-title {
            font-size: 48px;
            font-weight: 700;
            line-height: 56px;
            color: white;
            margin: 0;
        }

        &-link {
            display: flex;
            align-items: center;
            gap: 14px;
            font-size: 16px;
            font-weight: 500;
            color: white;
        }

        &-pagination {
            position: absolute;
            bottom: 40px;
            left: 350px;
            z-index: 1;
            display: flex;
            justify-content: space-between;
            align-items: center;
            gap: 2px;

            color: white;
            opacity: .5;
        }
    }

    &__form {
        display: flex;
        flex-direction: column;
        gap: 70px;
        padding: 72px 70px;

        border-radius: 32px;
        background-color: #F6F6F6;

        &-top {
            display: flex;
            flex-direction: column;
            gap: 16px;

            &-title {
                margin: 0;
                font-size: 32px;
                font-weight: 500;

                color: #3C3C3B;
            }

            &-description {
                font-size: 16px;
                color: #3C3C3B;
            }
        }

        &-content {
            width: 800px;
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
            gap: 32px 22px;

            &-item {
                display: flex;
                flex-direction: column;
                gap: 18px;
            }

            &-title {
                display: flex;
                align-items: center;
                gap: 8px;

                font-size: 12px;
                font-weight: 500;

                text-transform: uppercase;
                color: #3C3C3B;
            }

            &-field {
                display: flex;
                flex-direction: column;
                width: 324px;
                padding: 18px 24px;
                border-radius: 32px;
                border: none;
            }
        }

        &-bottom {
            display: flex;
            gap: 50px;
            justify-content: space-between;

            &-confirmation {
                width: 372px;
                font-size: 14px;
                color: #9A9A9A;
            }

            &-btn {
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

    &__mark {
        color: #719B2D
    }
}
</style>