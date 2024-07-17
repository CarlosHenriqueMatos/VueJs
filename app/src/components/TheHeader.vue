<template>
    <div>
        <div 
            v-for="(obj) in todos"
            :key = "obj.id"
            
            class="todos-item"
        >
        <!-- v-bind:key -->
        <img
            v-if= "obj.imgSrc"
            v-bind:src = "obj.imgSrc"
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
                }
            ]
        }
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