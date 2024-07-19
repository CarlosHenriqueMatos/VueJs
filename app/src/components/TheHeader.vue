<template>
    <div>
        <h2>Todos em aberto</h2>
        <div 
            v-for="obj in uncompletedTodos"
            :key = "obj.id"
            
            class="todos-item"
        >
        <input
            v-model="obj.completed"
            type="checkbox"
        >
        <!-- v-bind:key -->
        <img
            v-if= "obj.imgSrc"
            v-bind:src = "obj.imgSrc"
        >
        {{ obj.title }}
        </div>
        <h2>Todos completas</h2>
        <div 
            v-for="obj in completedTodos"
            :key = "obj.id"
            
            class="todos-item"
        >
        <input 
        v-model="obj.completed"
        type = "checkbox"
        >
        {{ obj.title }}
        </div>
    </div>
</template>

<script>


export default {
    name: 'App',
    data(){
      return{
        imgSrc: 'https://placehold.co/150',
        imgAlt: 'Foto Carlos',
        todos:[ 
                {
                "userId": 1,
                "id": 1,
                "title": "Econocargo",
                "completed": false
                },
                {
                "userId": 1,
                "id": 2,
                "title": "Conectando objetivos",
                "completed": false
                },
                {
                "userId": 1,
                "id": 3,
                "title": "XPTO",
                "completed": true
                },
                {
                "userId": 1,
                "id": 4,
                "title": "POT XT CAST",
                "completed": true
                }
            ]
        }
    }
,
computed:{
    uncompletedTodos(){
        return this.todos.filter(todo => !todo.completed);
    },
    completedTodos(){
        return this.todos.filter(todo => todo.completed);
    },
    },
methods:{

}
}
</script>


<style>
    .todos-item{
        background: #d8d2d2;
        margin: 0 0 5px 0;
        padding: 3px 6px;
    }
    .header {
        background: #dedcdc;
        color: #fff;
    }
</style>