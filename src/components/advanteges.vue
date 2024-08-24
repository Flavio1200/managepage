<script setup>
    defineProps(['number','title','content'])
</script>

<template>
    <div class="adv">
        <div class="item">
            <div class="nmb">{{ number }}</div>
        </div>
        <div class="item">
            <div class="text">
                <h4>{{ title }}</h4>
                <p>{{ content }}</p>
            </div>
        </div>
    </div>
</template>

<style scoped>
.adv{
    display: flex;
    justify-content: space-between;
    align-items: start;
    gap: 1rem;
    margin: 1rem 0;
}
.nmb{
    padding: .5rem 1rem;
    border-radius: 20px;
    background-color: #f25f3a;
    color: #fff;
}
h4{
    margin: 0;
}
</style>