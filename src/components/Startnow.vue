<script setup>
    import Button from "./Button.vue";
</script>

<template>
    <section class="start">
        <h2 class="title-start">Simplify how your team <br> works today.</h2>
        <div class="btn-cont"><Button style="color: #f25f3a; background-color: #fff;"/></div>
    </section>
</template>

<style scoped>
.start{
    background-image: url(../../public/images/bg-simplify-section-desktop.svg);
    background-color: var(--red);
    padding: 4rem 7rem;
}
.title-start{
    display: inline-block;
    color: #fff;
    font-size: 2rem;
}
.btn-cont{
    margin-top: 1rem;
    float: right;
}
</style>