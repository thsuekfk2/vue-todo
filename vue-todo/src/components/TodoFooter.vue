<template>
    <div class="clearAllContainer">
        <span class="ClearAllBtn" @click="clearTodo">Clear All</span>
    </div>
</template>
<script>
export default {
    methods:{
       clearTodo(){
           this.$emit('removeAll');
       } 
    }
}
</script>
<style scoped>

</style>