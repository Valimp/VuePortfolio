<script>
</script>

<template>
    <section id="{{ id }}" class="section">
        <slot></slot>
    </section>
</template>

<style scoped>
    .section {
        height: auto;
        background-color: #CCC9DC;
        color: #333232;
        clip-path: polygon(0 50px, 100% 0, 100% calc(100% - 50px), 0 100%);
        margin: 25rem 0;
        width: 100%;
        display: flex;
        flex-direction: column;
        padding: 10rem 15rem;
    }
</style>