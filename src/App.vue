<template>
  <EventPlannerHeader/>
  <EventsList :eventsList = eventsList />
</template>

<script>
  import EventPlannerHeader from "./components/EventPlannerHeader.vue";
  import EventsList from "./components/EventsList.vue";

  export default{
    name:"App",
    components:{
      EventPlannerHeader,
      EventsList
    },
    data(){
      return{
        eventsList:[]
      }
  },
  methods:{
    async fetchEventsList(){
      const response = await fetch("http://localhost:1597/api");
      const eventsData = await response.json();
      console.log(eventsData[0].events);
      return eventsData[0].events;
    },
  },
  async created(){
    this.eventsList = await this.fetchEventsList();
  }
  }
</script>

<style>
</style>