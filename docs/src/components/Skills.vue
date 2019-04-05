<template>
<div id="projects-container">
    <h2 v-on:click="displayInfo">Skills</h2>
    <div id="projects-info" v-if ="showInfo">
    <div class="view-item" v-for="skill in skills" :key="skill.title">
        <h3>{{skill.title}}</h3>
        <ul>
            <li v-for="skillItem in skill.skillSet" :key="skillItem">
                {{skillItem}}
            </li>
        </ul>
        </div>
    </div>
</div>
</template>

<script>
export default {
    name: 'skills',
    data(){
        return {
            showInfo: false,
            skills: [
                {
                    title: "Object Oriented Programming",
                    skillSet: [
                        "C#",
                        ".NET Framework"
                    ]
                },
                {
                    title: "Web Application Development",
                    skillSet: [
                        "ASP.NET MVC",
                        "HTML",
                        "CSS",
                        "JavaScript",
                        "VUE"
                    ]
                },
                {
                    title: "Database Programming",
                    skillSet: [
                        "SQL queries and DML",
                        "MSSQL"
                    ]
                },
                {
                    title: "Development Tools and Techniques",
                    skillSet: [
                        "Agile",
                        "unit testing (MStest)",
                        "integration testing",
                        "TDD",
                        "Unix command line navigation"
                    ]
                }
            ]
        }
        
        
    },
    methods: {
        /**
         * Toggles the display for the Skills section of the resume.
         */
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