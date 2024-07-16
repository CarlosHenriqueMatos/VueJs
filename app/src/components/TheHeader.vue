<template>
    <div>
        <div v-for="(obj, index) in todos"
            v-bind:key = "obj.id"
            class="todos-item"
        >
            {{ index+1 }} - {{ obj.title }}
        </div>
    </div>
</template>

<script>
export default {
    name: 'App',
    data(){
      return{
        todos:[ 
                {
                "userId": 1,
                "id": 1,
                "title": "Carlos Matos",
                "completed": false
                },
                {
                "userId": 1,
                "id": 2,
                "title": "Anna Matos",
                "completed": false
                },
                {
                "userId": 1,
                "id": 3,
                "title": "IFES",
                "completed": false
                },
                {
                "userId": 1,
                "id": 4,
                "title": "Ensino Médio, Superior e Mestrado",
                "completed": true
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