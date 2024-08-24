<script setup>
import Button from "./Button.vue";
</script>
<template>
    <main>
        <div class="part-main">
            <h1 class="title">Bring everyone <br> together to build <br> better products</h1>
            <p class="main-text">Manage makes it simple for software teams <br> to plan day-to-day tasks while keeping the <br> larger team goals in view.</p>
            <Button/>
        </div>
        <div class="part-main">
            <div class="img-cont">
                <img src="/images/illustration-intro.svg"/>
            </div>
        </div>
    </main>
</template>

<style scoped>
main{
    position: relative;
    padding: 1rem 2rem 2rem 2rem;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    align-items: center;
}
.part-main{
    flex: 1 1 375px;
}
.title{
    font-size: 4rem;
    font-weight: 600;
    margin: 0;
}
.main-text{
    font-size: 1.2rem;
    margin-top: .75rem;
    margin-bottom: 1.75rem;
}
.img-cont{
    min-width: 375px;
}
img{
    width: 100%;
}
</style>