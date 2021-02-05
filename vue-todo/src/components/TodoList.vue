<template>
    <section>
        <ul>
            <li v-for="(todoItem , index) in todoItems" v-bind:key="todoItem.id" class="shadow">
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
    data(){
        return{
            todoItems: []
        }
    },
     created(){
        if(localStorage.length > 0){
            for(var i=0; i < localStorage.length; i++){
               if(localStorage.key(i)!="loglevel:webpack-dev-server")
               this.todoItems.push(localStorage.key(i));
            }
        }
    },
    methods:{
        removeTodo(todoItem,index){
            localStorage.removeItem(todoItem);
            this.todoItems.splice(index, 1);
            // console.log(todoItem,index);
        }


    }
   
}
</script>
<style scoped>

</style>