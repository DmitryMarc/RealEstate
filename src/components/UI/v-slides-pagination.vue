<template>
    <font-awesome-icon 
        icon="angle-left" 
        :id="'swiper-prev'" 
        @click="onChangeSlide('prev')" 
        class="prev"
    />
    <span class="page">
        {{ currentPage }}
    </span>
    <span class="page">
        / {{ totalPages }}
    </span>
    <font-awesome-icon 
        icon="angle-right" 
        :id="'swiper-next'" 
        @click="onChangeSlide('next')" 
        class="next"
    />
</template>

<script>
export default {
    props:{
        currentPage: Number,
        totalPages: Number
    },
    methods:{
        onChangeSlide(value){
            this.$emit('onChangeSlide', value)
        }
    }
}
</script>

<style scoped lang="scss">
.prev,
.next{
    cursor: pointer;
}
.page{
    cursor: default;
}
</style>
