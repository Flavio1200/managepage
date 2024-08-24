<script setup>
defineProps(['avatar','name','experience'])
</script>

<template>
    <div class="card">
        <div class="avatar-cont">
            <img :src='avatar' alt="name">
        </div>
        <h4 class="name">{{ name }}</h4>
        <p class="exp">{{ experience }}</p>
    </div>
</template>

<style scoped>
.card{
    background-color: var(--light-gray);
}
.avatar-cont{
    width: 60px;
    margin: auto;
}
.avatar-cont> img{
    width: 100%;
}
h4{
    margin: 0;
    font-weight: 600;
}
.card{
    text-align: center;
    min-width: 350px;
    min-height: 250px;
    background-color: aliceblue;
    position: relative;
    display: flex;
    flex-direction: column;
    justify-content: end;
}

@media screen and (max-width: 375px) {
    .card{
        text-align: center;
        min-height: 250px;
        background-color: aliceblue;
        position: relative;
        display: flex;
        flex-direction: column;
        justify-content: end;
    }
}
</style>