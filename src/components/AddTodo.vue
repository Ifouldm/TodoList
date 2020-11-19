<template>
    <div class="navbar navbar-light bg-light mb-3">
        <form class="form-inline" @submit="addTodo">
            <div class="form-group">
                <input class="form-control flex-fill" type="text" name="title" v-model="title" placeholder="Add Todo...">
                <input class="btn btn-outline-success" type="submit" value="Submit">
            </div>
        </form>
    </div>
</template>

<script>
export default {
    name: "AddTodo",
    data() {
        return {
            title: ''
        }
    },
    methods: {
        addTodo(e) {
            e.preventDefault();
            const newTodo = {
                title: this.title,
                completed: false
            }
            // Send to parent
            this.$emit('add-todo',newTodo)
        }
    }

    
}
</script>

<style scoped>
</style>