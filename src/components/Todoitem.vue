<template>
<div class="todo-item" v-bind:class="{'is-completed': todo.complete === true}">
    <p class="item">
        {{todo.title}}
    </p>
    <button v-on:click="delItem" class="del">x</button>
    </div>  
</template>

<script>
export default {
    name: "TodoItem",
    props: {
        todo: Object
    },
    methods: {
        delItem(){
            console.log(this.todo.id);
        },
    },
}
</script>

<style scoped>
    .todo-item{
        background: #f4f4f4;
        padding: 10px;
        border-bottom: 1px #ccc dotted;
        display: flex;
        justify-content: space-between;
    }
   
    .is-completed {
        text-decoration: line-through;
    }
    .del {
   
        float: right;
        background: red;
        color: #fff;
        border-radius: 50%;
        border: none;
        width: 20px;
        height: 20px;
        line-height: 20px;
        cursor: pointer;
    }
</style>