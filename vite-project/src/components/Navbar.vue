<script setup lang="ts">
import { ref } from 'vue';
const nav = ['首页', '咨询', '快讯', '报告', '活动', '企业服务', '英文资讯']
const isActive = ref(false)
const toggle = () => { isActive.value = !isActive.value }
</script>

<template>
    <nav class="navbar">
        <div class="brand-title">Brand Name</div>
        <a href="#" class="toggle-button" @click="toggle">
            <span class="bar"></span>
            <span class="bar"></span>
            <span class="bar"></span>
        </a>
        <div class="navbar-links" :class="{ active: isActive }">
            <ul>
                <li><a href="#">Home</a></li>
                <li><a href="#">About</a></li>
                <li><a href="#">Contact</a></li>
            </ul>
        </div>
    </nav>
</template>

<style scoped>
.navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;

    background-color: #333;
    color: #fff;
}

.brand-title {
    font-size: 1.5rem;
    margin: .5rem 1rem;
}

.navbar-links ul {
    margin: 0;
    padding: 0;
    list-style-type: none;
    display: flex;
}

.navbar-links li a {
    text-decoration: none;
    color: #fff;
    padding: .5em 1em;
    display: block;
}

.navbar-links li:hover {
    background-color: #555;
}

.toggle-button {
    position: absolute;
    top: .75rem;
    right: .5rem;
    display: none;
    flex-direction: column;
    justify-content: space-between;
    width: 30px;
    height: 21px;
}

.toggle-button .bar {
    height: 3px;
    width: 100%;
    background-color: #fff;
    border-radius: 10px;
}

@media (max-width: 400px) {
    .toggle-button {
        display: flex;
    }

    .navbar-links {
        display: none;
        width: 100%;
    }

    .navbar {
        flex-direction: column;
        align-items: flex-start;
    }

    .navbar-links ul {
        width: 100%;
        flex-direction: column;
    }

    .navbar-links li {
        text-align: center;
    }

    .navbar-links.active {
        display: flex;
    }
}
</style>