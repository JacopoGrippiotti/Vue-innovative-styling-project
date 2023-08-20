<template>
    <AppHeader @changedValue="apiCall"/>
    <div class="container">
        <div>
            {{ response }}
        </div>
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
                    this.response += " "
                    
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
    
    div.container{
        display: flex;
        justify-content: center;
        margin: 0 auto;
        
    }
   
</style>