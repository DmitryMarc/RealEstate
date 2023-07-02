<template>
    <div class="card">
        {{ house1 }}
        <img src="../assets/img/cards/house1.png" alt="фото" class="card__img" />
        <div class="card__info">
            <h3 class="card__info-title">
                {{ item.title }}
            </h3>
            <span class="card__info-price">
                от {{ item.price }} млн. ₽
            </span>
        </div>
        <span class="card__location">
            <font-awesome-icon icon="location-dot" />
            <span class="card__location-text">
                {{ item.location }}
            </span>
        </span>
    </div>
</template>

<script>
export default{
    props:{
        item:{
            id: String,
            title: String,
            imgUrl: String,
            price: Number,
            location: String
        }
    },
    computed: {
        imageSrc() {
            return `../assets/img/cards/${this.item.imgUrl}`;
        }
  }
}

</script>

<style scoped lang="scss">
.card{
    display: flex;
    flex-direction: column;
    gap: 16px;
    width: 31%;
    flex-grow: 1;

    &:last-child{
        max-width: 45%;
    }

    &__img{
        width: 100%;
    }

    &__info{
        display: flex;
        justify-content: space-between;
        align-items: center;

        &-title{
            margin: 0;
            font-size: 24px;
            font-weight: 700;
            color: #3C3C3B;
        }

        &-price{
            font-size: 20px;
            font-weight: 700;
            color: #3C3C3B;
        }
    }

    &__location{
        display: flex;
        align-items: baseline;
        gap: 8px;

        &-text{
            font-size: 18px;
            font-weight: 500;
            color: #9A9A9A;
        }
    }
}

</style>