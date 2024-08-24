<script setup>
import { ref } from 'vue'
import Button from './Button.vue'
const isAct = ref(false);
</script>

<template>
    <header class="head">
        <nav class="navbar">
            <div class="part">
                <img src="/images/logo.svg" alt="logo">
            </div>
            <ul class="part">
                <li><a href="#" class="link">Pricing</a></li>
                <li><a href="#" class="link">Products</a></li>
                <li><a href="#" class="link">About us</a></li>
                <li><a href="#" class="link">Careers</a></li>
                <li><a href="#" class="link">Comunuty</a></li>
            </ul>
            <div class="part">
                <Button/>
            </div>
        </nav>
        <nav class="navbar-mobile">
            <div class="part">
                <img src="/images/logo.svg" alt="logo">
            </div>
            <ul class="part-mobile" :class="{active: isAct}">
                <li><a href="#" class="link">Pricing</a></li>
                <li><a href="#" class="link">Products</a></li>
                <li><a href="#" class="link">About us</a></li>
                <li><a href="#" class="link">Careers</a></li>
                <li><a href="#" class="link">Comunuty</a></li>
            </ul>
            <div class="part" @click="isAct = !isAct">
                <img src="/images/icon-hamburger.svg" alt="menu">
            </div>
        </nav>

    </header>
</template>
<style scoped>
.head{
    padding: 2rem 2.5rem;
}
.navbar{
    position: relative;
    display: flex;
    justify-content: space-between;
    align-items: center;
}
.part{
    padding: 0;
    list-style-type: none;
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 2rem;
}
.link{
    color: #242d52;
}
.navbar-mobile{
    display: none;
}
@media screen and (max-width: 375px) {
    .navbar{
        display: none;
    }
    .navbar-mobile{
        display: flex;
        justify-content: space-between;
        align-items: center;
        position: relative;
    }
    .part-mobile{
        position: absolute;
        border-radius: 8px;
        z-index: 1000;
        top: 0;
        left: 50%;
        width: 100%;
        background-color: #242d52;
        text-align: center;
        list-style-type: none;
        transform: translateX(-50%) translateY(-150%);
        transition: all .5s ease-in-out;
    }
    .part-mobile.active{
        transform: translateY(50%) translateX(-50%);
    }
    .part-mobile>li{
        margin-block: 1rem;
    }
    .part-mobile>li>a{
        color: #fff;
    }
}
</style>

