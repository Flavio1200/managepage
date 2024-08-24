<script setup>
import { ref } from 'vue'
import Cards from './Cards.vue'
import clients from '../../data/clients.json'
const c = ref(clients)
</script>

<template>
    <section class="testimonies">
        <h2> What they’ve said</h2>
        <div class="testimonies-container">
            <Cards v-for="client in c" :key="client.name" :avatar="client.avatar" :name="client.name" :experience="client.experience"/>
        </div>
    </section>
</template>

<style scoped>
.testimonies{
    padding: 2rem 5rem;
}
h2{
    text-align: center;
}
.testimonies-container{
    overflow-x: scroll;
    padding: .5rem;
    /* margin: .75rem; */
    width: inherit;
    background-color: var(--blanco-puro);
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 1rem;
}

@media screen and (max-width: 375px) {
    .testimonies{
        padding: 1rem;
    }
    .testimonies-container{
        overflow: hidden;
        flex-direction: column;
    }
}
</style>