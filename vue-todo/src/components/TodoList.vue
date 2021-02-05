<template>
    <section>
        <ul>
            <li v-for="(todoItem , index) in propsdata" v-bind:key="todoItem" class="shadow">
                <i class="checkBtn fas fa-check" aria-hidden="true"></i>    
                {{todoItem}}
                <span class="removeBtn" type="button" @click="removeTodo(todoItem,index)">
                    <i class="far fa-trash-alt" aria-hidden="true"></i>
                    </span>
                        </li> 
        </ul>

    </section>
</template>
<script>
export default {
    props:['propsdata'],
   


    methods:{
        removeTodo(todoItem,index){
           this.$emit('removeTodo',todoItem,index);
        },
        


    }
   
}
</script>
<style scoped>

</style>