<template>

    <div>
        <div v-bind:key="todo.id" v-for="todo in todos">
            <TodoItem v-bind:todo="todo" v-on:del-todo="$emit('del-todo',todo.id)"/>
            <!-- <h3>{{todo.title}}</h3> -->
        </div>
    </div>
</template>

<script>
import TodoItem from './TodoItem.vue'

export default {
    name : "Todos",
    props : ["todos"], // App.vueでlink
    components: {
        TodoItem
    },
}
</script>

<style scoped>


</style>