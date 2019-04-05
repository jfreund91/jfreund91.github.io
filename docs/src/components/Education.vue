<template>
<div id="education-container">
    <h2 v-on:click="displayInfo">Education</h2>
    <div id="edu-info" v-if ="showInfo">
    <div class="education-item" v-for="school in schools" :key="school.id">
        <img v-bind:src="school.imgSrc" class="school-logo"/>
        <h3>{{school.institution}}</h3>
        <h4>{{school.fieldOfStudy}}</h4>
        <p>{{school.description}}</p>
        </div>
    </div>
</div>
</template>

<script>
export default {
    name: 'education',
    data(){
        return {
            showInfo: false,
        schools: [
                {
                    id: 2,
                    institution: "Tech Elevator",
                    fieldOfStudy: ".NET Development Boot-camp",
                    description: "Attending a 14-week coding boot-camp learning how to develop dynamic web based applications using the .NET Framework.",
                    imgSrc: require('@/assets/techelevator.png')
                },
                {
                    id: 1,
                    institution: "The University of Akron",
                    fieldOfStudy: "Biomedical Engineering",
                    description: "Various coursework completed.",
                    imgSrc: require('@/assets/uakron.png')
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
.school-logo {
    width: 156px;
    height: auto;
}
.education-item {
    border: 5px darkblue solid;
    margin: 0 0 10px 0;
    padding: 10px 0 10px 0;
    background-color: lightblue;
}
</style>
