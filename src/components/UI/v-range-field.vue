<template>
    <vue-slider 
        v-model="value" 
        @change="onChange"
        :tooltipPlacement="'bottom'" 
        :tooltip-formatter="'{value} млн. руб.'" 
        :enableCross="false" 
        :process="process"
        :width="'90%'"
        :process-style="{ backgroundColor: '#719B2D' }"
        :interval="0.1"
        :min="minValue"
        :max="maxValue"
        class="range"
    />
</template>

<script>
import VueSlider from 'vue-slider-component'
import 'vue-slider-component/theme/antd.css'

export default {
    props:{
        rangeValue: Array,
    },
    components: {
        VueSlider,
    },
    data() {
        return {
            value: this.rangeValue,
            minValue: null,
            maxValue: null
        }
    }, 
    methods:{
        onChange(){
            this.$emit('onChange', this.value)
        }
    },
    created(){
        this.minValue = this.rangeValue[0];
        this.maxValue = this.rangeValue[1];
    }
}
</script>

<style scoped lang="scss">
.range{
    position: absolute;
    bottom: -6px;
    left: 24px;
}
</style>