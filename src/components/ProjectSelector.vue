<template>
    <v-flex xs3>
        <v-select
            v-model="selectedProject"
            :items="projects"
            item-text="name"
            item-value="name"     
            class="mr-5"   
        ></v-select>
    </v-flex>
</template>
<script>
import axios from '../../node_modules/axios/dist/axios.min'
import config from '../config/Configuration'

export default {
    name: 'ProjectSelector',
    data() {
        return {
            selectedProject: null,
            projects: []
        }
    },
    mounted() {
        axios
        .get(config.apiBaseUrl + 'projects/')
        .then(response => {
            this.projects = response.data._embedded.projects;
            this.selectedProject = this.projects[0].name;
        })
    }      
}
</script>