<template>
    <div class="list">
    <div class="title">
    <h3>Список дел на сегодня</h3>
    </div>
    <div class="doings">
    <ul>
        <li class='item' v-for="(todo, index) in todos" v-on:click="deleteTodo(index)" v-bind:key="index">{{ todo }}</li>
    </ul>
    </div>
    </div>
</template>

<script>
export default {
    props: ['todos'],
    methods: {
        deleteTodo(index){
            this.$emit('delete-todo', index);
        }
    }
}
</script>