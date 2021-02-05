<template>
    <div class="clearAllContainer">
        <span class="ClearAllBtn" @click="clearTodo">Clear All</span>
    </div>
</template>
<script>
export default {
    methods:{
       clearTodo(){
           localStorage.clear();
       } 
    }
}
</script>
<style scoped>

</style>