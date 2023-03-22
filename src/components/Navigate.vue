<script>
import { ref } from 'vue';
export default {
    setup(){
        let isOpen = ref(false)
        function handleMenu() {
            isOpen.value = !isOpen.value
            console.log(isOpen.value);
        }
        return {isOpen, handleMenu}
    }
}
</script>

<template>
    <header class="header">
        <h1 class="title">
            PhotoCM
        </h1>
        <nav class="menu" :class="{ showMenu: isOpen }">
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
            <button @click="handleMenu()" class="burger-box">
                <span class="burger"></span>
            </button>
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
    .burger-box {
        width: 20px;
        height: 20px;
        background-color: transparent;
        color: inherit;
        display: none;
    }

    @media screen and (max-width: 920px) {
        .links {
            display: none;
        }
        .burger-box {
            display: block;
            z-index: 10;
            border: none;
        }
        .burger-box:hover {
            cursor: pointer;
        }
        .burger,
        .burger::before,
        .burger::after {
            align-self: center;
            display: block;
            width: 20px;
            height: 2px;
            background-color: white;
            border-radius: 1px;
            position: relative;
            transition: all .5s ease-in-out;
        }
        .burger::before,
        .burger::after {
            content: '';
            position: absolute;
            left: 0;
        }
        .burger::before {
            transform: translateY(-6px);
            width: 15px;
        }
        .burger::after {
            transform: translateY(6px);
            width: 15px;
        }
        .showMenu .burger {
            width: 0;
            background: transparent;
        }
        .showMenu .burger::before {
            width: 20px;
            transform: rotate(45deg);
        }
        .showMenu .burger::after {
            width: 20px;
            transform: rotate(-45deg);
        }
    }
</style>