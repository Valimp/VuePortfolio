<script>
</script>

<template>
    <header class="header">
        <h1 class="title">
            PhotoCM
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
        z-index: 5;
        color: white;
    }
    .title {
        font-family: 'Delicious Handrawn', cursive;
    }
    .links {
        display: flex;
    }
    .link {
        list-style-type: none;
        margin: 0 20px;
        transform: all .2s;
    }
    .link a {
        color: white;
        position: relative;
    }
    .link  a::after {
        content: '';
        height: 1.5px;
        background-color: orange;
        transform-origin: 0 0;
        position: absolute;
        bottom: -2px;
        left: 0;
        right: 0;
        transform: scaleX(0);
        transition: transform .4s ease-in-out;
        border-radius: 1px;
    }
    .link a:hover::after {
        transform: scaleX(1);
    }
</style>