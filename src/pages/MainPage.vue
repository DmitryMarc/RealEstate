<template>
    <v-header />
    <ConsultationForm />
    <ProjectsBlock />
    <v-footer />
</template>

<script>
import VHeader from '../components/v-header.vue';
import ConsultationForm from '../components/СonsultationForm.vue';
import ProjectsBlock from '../components/ProjectsBlock.vue';
import VFooter from '../components/v-footer.vue';

export default {
    components:{
        VHeader,
        ConsultationForm,
        ProjectsBlock,
        VFooter
    }
}

</script>