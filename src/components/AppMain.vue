<template>
    ciao
</template>
<script>
import axios from 'axios';
export default {
    name:'AppMain',
    data() {
        return {
            apiUrl:'https://flynn.boolean.careers/exercises/api/random/word',
            response:[],
        }
    },
    methods: {
        apiCall(){
            axios.get(this.apiUrl).then(
                (response) => {
                    this.response = response.data.response
                    console.log(this.response)
                }
            )

            
        }
    },
    mounted(){
        this.apiCall()
    },
}
</script>
<style lang="scss" scoped>
    @use '../styles/partials/mixins' as*;
    @use '../styles/partials/variables' as*;
</style>