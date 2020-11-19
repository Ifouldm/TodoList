<template>
    <div class="d-flex justify-content-between">
        <input class="checkbox-inline check" type="checkbox" v-bind:checked="todo.completed" v-on:change="markComplete">
        <div v-bind:class="{'is-complete':todo.completed}">{{todo.title}}</div>
        <button class="btn btn-danger btn-lg" @click="$emit('del-todo',todo.id)"><font-awesome-icon :icon="myIcon" /></button>
    </div>
</template>

<script>
import {FontAwesomeIcon } from '@fortawesome/vue-fontawesome'
import { faTrash } from '@fortawesome/free-solid-svg-icons'

export default {
    name: "TodoItem",
    props: ["todo"],
    methods: {
        markComplete() {
            this.todo.completed = ! this.todo.completed;
        }
    },
    data () {
    return {
      myIcon: faTrash
    }
  },
  components: {
      FontAwesomeIcon
  }
}
</script>

<style scoped>
    .is-complete {
        text-decoration: line-through;
    }
    .check {
        width: 50px;
        height: 50px;
    }
</style>