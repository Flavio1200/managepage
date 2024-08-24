<script setup>
import advanteges from './advanteges.vue';
</script>

<template>
    <section class="info">
        <div class="info-part">
            <h2 class="title-info">What's different about <br> Manage?</h2>
            <p>
                Manage provides all the functionality your team needs, without 
                the complexity. Our software is tailor-made for modern digital 
                product teams.
            </p>
        </div>
        <div class="info-part">
            <advanteges 
                number="01" 
                title="Track company-wide progress" 
                content="See how your day-to-day tasks fit into the wider vision. Go from 
                        tracking progress at the milestone level all the way done to the 
                        smallest of details. Never lose sight of the bigger picture again."
            />
            <advanteges 
            number="02" 
            title="Advanced built-in reports"
            content="Set internal delivery estimates and track progress toward company 
                    goals. Our customisable dashboard helps you build out the reports 
                    you need to keep key stakeholders informed."
            />
            <advanteges 
            number="03" 
            title="Everything you need in one place"
            content="Stop jumping from one service to another to communicate, store files, 
                    track tasks and share documents. Manage offers an all-in-one team 
                    productivity solution."
            />
        </div>
    </section>
</template>

<style scoped>
.info{
    padding: 2rem 5rem;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    align-items: start;
    gap: 3rem;
}
.info-part{
    flex: 1 1 300px;
}
.title-info{
    font-size: 2.5rem;
    margin: 0;
    padding-bottom: 1rem;
}
</style>