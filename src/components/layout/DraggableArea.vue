<template>
    <div class="draggable">
        DraggableArea
    </div>
</template>

<script>
export default {
    name: "DraggableArea"
}
</script>

<style scoped>
    .draggable {
        -webkit-app-region: drag;
        width: 100%;
        position: fixed;
        bottom: 0;
        height: 50px;
        background-color: #fff;
    }
</style>