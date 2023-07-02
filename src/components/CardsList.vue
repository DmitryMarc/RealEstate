<template>
    <div class="list">
        <ListItem v-for="item in list" :key="item.id" :item="item" />
    </div>
</template>

<script>
import ListItem from './ListItem.vue';

export default{
    components:{
        ListItem
    },
    data(){
        return {
            list: [
                {
                    id: '0',
                    title: 'Название проекта',
                    imgUrl: 'house1.png',
                    price: 3.1,
                    location: 'Санкт-Петербург'
                },
                {
                    id: '1',
                    title: 'Название проекта',
                    imgUrl: '#',
                    price: 3.1,
                    location: 'Санкт-Петербург'
                },
                {
                    id: '2',
                    title: 'Название проекта',
                    imgUrl: '#',
                    price: 3.1,
                    location: 'Санкт-Петербург'
                },
                {
                    id: '3',
                    title: 'Название проекта',
                    imgUrl: '#',
                    price: 3.1,
                    location: 'Санкт-Петербург'
                },
                {
                    id: '4',
                    title: 'Название проекта',
                    imgUrl: '#',
                    price: 3.1,
                    location: 'Санкт-Петербург'
                },
                {
                    id: '5',
                    title: 'Название проекта',
                    imgUrl: '#',
                    price: 3.1,
                    location: 'Санкт-Петербург'
                },
                {
                    id: '6',
                    title: 'Название проекта',
                    imgUrl: '#',
                    price: 3.1,
                    location: 'Санкт-Петербург'
                },
                {
                    id: '7',
                    title: 'Название проекта',
                    imgUrl: '#',
                    price: 3.1,
                    location: 'Санкт-Петербург'
                },
            ]
        }
    }
}

</script>

<style scoped lang="scss">

.list{
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 40px 24px;
}
</style>
