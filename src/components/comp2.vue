<template>

    <div id="todo-list-example">
        <form v-on:submit.prevent="addNewTodo">
            <label for="newtodo">Add a todo</label>
            <input
                    v-model="newTodoText"
                    id="newtodo"
                    placeholder="E.g. Feed the cat"
            >
            <button>Add</button>
        </form>
        <ul>
            <td1
                    v-for="(todo, index) in todos"
                    v-bind:key="todo.id"
                    v-bind:title="todo.title"
                    v-on:remove="todos.splice(index, 1)"
            ></td1>
        </ul>
    </div>
</template>


<script>
    import td1 from './td1.vue'

    export default {
        name: "comp2",
        component:{td1},
        //el: '#todo-list-example',
        data: function () {
            return {
                newTodoText: '',
                todos:
                    [
                        {
                            id: 1,
                            title: 'Do the dishes',
                        },
                        {
                            id: 2,
                            title: 'Take out the trash',
                        },
                        {
                            id: 3,
                            title: 'Mow the lawn'
                        }
                    ],
                nextTodoId:
                    4
            }
        },
        methods: {
            addNewTodo: function () {
                this.todos.push({
                    id: this.nextTodoId++,
                    title: this.newTodoText
                })
                this.newTodoText = ''
            }
        }
    }
</script>
<style scoped>

</style>