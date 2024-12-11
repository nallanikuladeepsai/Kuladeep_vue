<template>
    <div class="event_card">
        <div class="event_photo">
            <img :src=event.event_image_url alt="Event Photo"/>
        </div>
    <div>
        <h3>{{event.event_name}}</h3>
        <p class="gray"><img src="https://img.icons8.com/?size=20&id=85149&format=png" alt="Location Icon"/> {{event.event_location}}</p>
        <hr>
        <div class="flex-container">
            <p><img src="https://img.icons8.com/?size=20&id=85102&format=png&color=000000"/> {{event.event_date}}</p>
            <p><img src="https://img.icons8.com/?size=20&id=83147&format=png&color=000000"/> {{event.event_time}}</p>
        </div>
        <p>{{event.event_description}}</p>
    </div>
     </div>
</template>

<script>
    export default{
        name: "SingleEvent",
        props:{
            event: Object
        },
    }
</script>

<style scoped>
.event_card{
        display:flex;
        flex-direction:column;
        justify-content:space-between;
        align-content:center;
        border:transparent;
        border-radius:4px;
        padding:10px;
        box-shadow:0 4px 8px 0 rgba(0,0,0,0.2), 0 6px 20px 0 rgba(0,0,0,0.19);
    }
.event_photo{
        width:100%;
    }
.event_photo img{
        width:100%;
        height:250px;
    }
.flex-container{
        display:flex;
        justify-content:space-between;
        align-items:center;
}
.flex-container img{
    vertical-align:middle; 
}
.gray img{
    vertical-align:middle;
}
</style>