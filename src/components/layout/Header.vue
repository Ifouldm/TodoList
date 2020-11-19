<template>
    <header>
        <h1 class="jumbotron display-4 m-0">TodoList</h1>
        <nav class="navbar navbar-light bg-light mb-3d" id="nav">
            <router-link class="nav-item nav-link" to="/">Home</router-link>
            <router-link class="nav-item nav-link" to="/about">About</router-link>
        </nav>
    </header>
</template>

<script>
export default {
    name: "Header"
}
</script>

<style scoped>
</style>