<script setup lang="ts">
import { ref } from 'vue'
const isActive = ref(false)
const toggle = () => { isActive.value = !isActive.value }
</script>

<template>
    <nav>
        <ul class="menu">
            <li class="logo"><a href="#">FollowAndrew.dev</a></li>
            <li :class="{ active: isActive }" class="item"><a href="#">Home</a></li>
            <li :class="{ active: isActive }" class="item"><a href="#">About</a></li>
            <li :class="{ active: isActive }" class="item"><a href="#">Service</a></li>
            <li :class="{ active: isActive }" class="item button"><a href="#">Login</a></li>
            <li :class="{ active: isActive }" class="item button secondary"><a href="#">Sign Up</a></li>
            <li class="toggle" @click="toggle"><span class="bars"></span></li>
        </ul>

    </nav>
</template>

<style scoped>
nav {
    background-color: #222;
    padding: 5px 20px;
}

a {
    color: #fff;
}

a:hover {
    text-decoration: underline;
}

.menu li {
    font-size: 16px;
    padding: 15px 5px;
}

.menu li a {
    display: block;
}

.menu .logo {
    font-size: 20px;
}

.button.secondary {
    border-bottom: 1px solid #444;
}

/* 移动端样式 */
.menu {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    align-items: center;
}

.toggle {
    order: 1;
}

.item.button {
    order: 2;
}

.item {
    width: 100%;
    text-align: center;
    order: 3;
    display: none;
}

.item.active {
    display: block;
}

.toggle {
    cursor: pointer;
}

.bars {
    background-color: #999;
    display: inline-block;
    height: 2px;
    position: relative;
    width: 18px;
    vertical-align: middle;
}

.bars::before,
.bars::after {
    background-color: #999;
    content: '';
    display: inline-block;
    height: 2px;
    position: absolute;
    width: 18px;
}

.bars::before {
    top: 5px;
}

.bars::after {
    top: -5px;
}

/* 平板设备 */
@media all and (min-width:468px) {
    .menu {
        justify-content: center;
    }

    .logo {
        flex: 1;
    }

    .item.button {
        display: block;
        order: 1;
        width: auto;
    }

    .toggle {
        order: 2;
    }

    .button.secondary {
        border: 0;
    }

    .button a {
        padding: 7px 15px;
        background-color: teal;
        border: 1px solid #006d6d;
        border-radius: 50em;
    }

    .button.secondary a {
        background: transparent;
    }

    .button a:hover {
        transition: all .25s;
    }

    .button:not(.secondary) a:hover {
        background-color: #006d6d;
        border-color: #005959;
    }

    .button.secondary a:hover {
        color: #ddd;
    }
}

/* 桌面端设备 */
@media all and (min-width: 768px) {
    .item {
        display: block;
        width: auto;
    }

    .toggle {
        display: none;
    }

    .logo {
        order: 0;
    }

    .item {
        order: 1;
    }

    .button {
        order: 2;
    }

    .menu li {
        padding: 15px 10px;
    }

    .menu li.button {
        padding-right: 0;
    }
}
</style>