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
                    <a href="#about">Qui suis-je ?</a>
                </li>
                <li class="link">
                    <a href="#portfolio">Portfolio</a>
                </li>
                <li class="link">
                    <a href="#offer">Mes offres</a>
                </li>
                <li class="link">
                    <a href="#contact">Me contacter</a>
                </li>
            </ul>
            <span class="burger"></span>
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
        background-color: #333232;
        position: sticky;
        top: 0;
        left: 0;
        z-index: 5;
        color: white;
    }
    .title {
        font-family: 'Delicious Handrawn', cursive;
    }
    .menu {
        display: flex;
        align-items: center;
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
    .burger,
    .burger::before,
    .burger::after {
        width: 20px;
        height: 2px;
        background-color: white;
        border-radius: 1px;
        position: relative;
    }
    .burger::after,
    .burger::before {
        content: '';
        position: absolute;
        left: 0;
    }
    .burger::before {
        transform: translateY(-6px);
    }
    .burger::after {
        transform: translateY(6px);
    }

    @media screen and (max-width: 920px) {
        .links {
            display: none;
        }
    }
</style>