<template>
<div class="grid-container">
    <div v-for="event of eventsList" :key="event.event_name">
        <SingleEvent :event = event />
    </div>
</div>
</template>

<script>
import SingleEvent from "./SingleEvent.vue";

export default{
    name:"EventsList",
    components:{
        SingleEvent
    },
    props:{
        eventsList:Array
    }
}
</script>

<style>
.grid-container{
    display: grid;
    grid-template-columns: auto auto auto;
    gap:2em;
}
</style>