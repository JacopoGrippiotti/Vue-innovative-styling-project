<template >
    <div>
        <select v-model="numberOfWords" @change="$emit('changedValue',numberOfWords)" name="numberOfWords" id="numberOfWords" >
            <option value="1" selected>1</option>
            <option value="2">2</option>
            <option value="3">3</option>
        </select>
        {{ numberOfWords }}
    </div>
</template>

<script>
export default {
    name:'AppHeader',
    
  data() {
    return {
        numberOfWords: ''
    }
  },    
}
</script>

<style lang="scss" scoped>
    @use '../styles/partials/mixins' as*;
    @use '../styles/partials/variables' as*;

</style>