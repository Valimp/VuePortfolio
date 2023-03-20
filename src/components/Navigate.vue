<script>
</script>

<template>
    <header class="header">
        <h1>
            CMPhoto
        </h1>
        <nav class="menu">
            <ul class="links">
                <li class="link">
                    <a href="#">Qui suis-je ?</a>
                </li>
                <li class="link">
                    <a href="#">Portfolio</a>
                </li>
                <li class="link">
                    <a href="#">Mes offres</a>
                </li>
                <li class="link">
                    <a href="#">Me contacter</a>
                </li>
            </ul>
        </nav>
    </header>
</template>

<style scoped>
    .header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        width: 100%;
        padding: 10px 20px;
        background-color: #0000006b;
        position: sticky;
        top: 0;
        left: 0;
    }
    .links {
        display: flex;
    }
    .link {
        list-style-type: none;
        margin: 0 20px;
    }
</style>