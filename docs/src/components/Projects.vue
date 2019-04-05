<template>
<div id="projects-container">
    <h2 v-on:click="displayInfo">Projects</h2>
    <div id="projects-info" v-if ="showInfo">
    <div class="view-item" v-for="project in projects" :key="project.id">
        <h3>{{project.title}}</h3>
        <h4>{{project.description}}</h4>
        </div>
    </div>
</div>
</template>

<script>
export default {
    name: 'projects',
    data(){
        return {
            showInfo: false,
            projects: [
                {
                    id: 1,
                    title: "Vending Machine Software",
                    description: "Designed a virtual vending machine using  OOP fundamentals  and TDD techniques using File I/O. "
                },
                {
                    id: 2,
                    title: "National Park Campsite Reservation System",
                    description: "Developed in C# and MSSQL using system integration techniques."
                },
                {
                    id: 3,
                    title: "National Park Weather Service",
                    description: "Designed and implemented a dynamic ASP.NET Core web  application that retrieves forecasts, stores user reviews, and  ranked the parks by the scores."
                },
                {
                    id: 4,
                    title: "Board Game Library",
                    description: "Worked in parallel to design and implement an ASP.NET  dynamic web application for displaying, adding, and browsing  games from an integrated database on a team of four."
                }
            ]
        }
        
        
    },
    methods: {
            displayInfo() {
                if(this.showInfo === false) {
                    this.showInfo = true;
                } else {
                    this.showInfo = false;
                }
            }
        }
}
</script>

<style>
.view-item {
    border: 5px darkblue solid;
    margin: 0 0 10px 0;
    padding: 10px 0 10px 0;
    background-color: lightblue;
}
h3 {
    font-size: 24px;
}
</style>
