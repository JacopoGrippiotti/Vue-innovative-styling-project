<template>
    <AppHeader @changedValue="apiCall"/>
    <div>
        {{ response }}
    </div>
</template>
<script>
import axios from 'axios';
import AppHeader from './AppHeader.vue';
export default {
    name:'AppMain',
    components:{
        AppHeader
    },
    data() {
        return {
            apiUrl:'https://flynn.boolean.careers/exercises/api/random/word',
            response:"",
        }
    },
    methods: {
        apiCall(numberOfWords){
            for(let i = 0; i<numberOfWords; i++){
            axios.get(this.apiUrl).then(
                (response) => {
                    this.response += response.data.response
                    console.log(this.response)
                }
            )    
        }
    },
    mounted(){
        this.apiCall()
    },
 }
}
</script>
<style lang="scss" scoped>
    @use '../styles/partials/mixins' as*;
    @use '../styles/partials/variables' as*;
</style>