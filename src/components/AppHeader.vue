<template >
    <div>
        <select v-model="numberOfWords"  name="numberOfWords" id="numberOfWords" >
            <option @click="$emit('changedValue',numberOfWords)" value="1" selected>1</option>
            <option @click="$emit('changedValue',numberOfWords)" value="2">2</option>
            <option @click="$emit('changedValue',numberOfWords)" value="3">3</option>
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