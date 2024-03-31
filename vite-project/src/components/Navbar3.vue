<script setup lang="ts">
import { ref } from 'vue'

const navigation = ['Home', 'About', 'Contact', 'Project']

const isActive = ref(false)
const toggle = () => { isActive.value = !isActive.value }
</script>

<template>
    <nav>
        <div class="logo">
            <h4>The Nav</h4>
        </div>
        <ul class="nav-links" :class="{ 'nav-active': isActive }">
            <li v-for="nav, idx of navigation" :style="{ animation: `navLinkFade 0.5s ease forwards ${idx / 7 + 2}s` }">
                <a href="#">
                    {{ nav }}
                </a>
            </li>
        </ul>
        <div class="burger" @click="toggle">
            <div class="line1"></div>
            <div class="line2"></div>
            <div class="line3"></div>
        </div>
    </nav>
</template>

<style scoped>
nav {
    display: flex;
    justify-content: space-around;
    align-items: center;
    min-height: 8vh;
    background-color: #5d4954;
}

.logo {
    color: #fff;
    text-transform: uppercase;
    letter-spacing: 5px;
    font-size: 20px;
}

.nav-links {
    display: flex;
    /* background-color: red; */
    justify-content: space-around;
    width: 30%;
}

.nav-links li {
    list-style-type: none;
}

.nav-links a {
    text-decoration: none;
    color: #fff;
    letter-spacing: 3px;
    font-weight: bold;
    font-size: 14px;
}

.burger {
    display: none;
    cursor: pointer;
}

.burger div {
    width: 25px;
    height: 3px;
    background-color: #fff;
    margin: 5px;
}

@media screen and (max-width: 1024px) {
    .nav-links {
        width: 60%;
    }
}

@media screen and (max-width: 768px) {
    body {
        overflow-x: hidden;
    }

    .nav-links {
        position: absolute;
        right: 0;
        top: 8vh;
        height: 92vh;
        background-color: #5d4954;
        display: flex;
        flex-direction: column;
        align-items: center;
        width: 50%;
        transform: translateX(100%);
        transition: transform 0.5s ease-in;
    }

    .nav-links li {
        opacity: 0;
    }

    .burger {
        display: block;
    }

    .nav-active {
        transform: translateX(0);
    }
}

@keyframes navLinkFade {
    from {
        opacity: 0;
        transform: translateX(50px);
    }

    to {
        opacity: 1;
        transform: translateX(0);
    }
}
</style>