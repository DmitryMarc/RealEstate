<template>
    <v-header />
    <ConsultationForm />
    <ProjectsBlock />
</template>

<script>
import VHeader from '../components/v-header.vue';
import ConsultationForm from '../components/СonsultationForm.vue';
import ProjectsBlock from '../components/ProjectsBlock.vue';

export default {
    components:{
        VHeader,
        ConsultationForm,
        ProjectsBlock,
    }
}

</script>