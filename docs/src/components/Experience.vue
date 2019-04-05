<template>
<div id="projects-container">
    <h2 v-on:click="displayInfo">Previous Work Experience</h2>
    <div id="projects-info" v-if ="showInfo">
    <div class="view-item" v-for="exp in experience" :key="exp.company">
        <h3>{{exp.company}}</h3>
        <h4>{{exp.position}}</h4>
        <h5>{{exp.time.start}} to {{exp.time.finish}}</h5>
        <ul>
            <li v-for="responsibility in exp.responsibilities" :key="responsibility">{{responsibility}}</li>
        </ul>
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
            experience: [
                {
                    company: "Inogen",
                    position: "DTP Sales Representative",
                    time: {
                        start: "March 2018",
                        finish:"July 2018"
                    },
                    responsibilities: [
                        "Collaborated with multiple departments to provide full  service patient care (Billing, Patient Care, On-Call  Respiratory Therapists)",
                        "Coordinated communication between physicians,  insurance companies, government agencies and  patients.",
                        "Analyzed and approved patient medical records."
                    ]
                },
                {
                    company: "Tailored Brands, Inc.",
                    position: "Wardrobe Consultant",
                    time: {
                        start: "July 2010",
                        finish: "September 2017"
                    },
                    responsibilities: [
                        "Trained new consultants in product knowledge and proper fitting technique.",
                        "Led region-wide training exercises in best practices and sales behaviors.",
                        "Built strong relationships with repeat customers and developed a clientele."
                    ]
                },
                {
                    company: "Medical Specialties Distributors, LLC",
                    position: "Warehouse Associate",
                    time: {
                        start: "June 2012",
                        end: "July 2014"
                    },
                    responsibilities: [
                        "Developed and implemented a new product organization system that increased order output.",
                        "Managed internal logistics to ensure timely and accurate product delivery."
                    ]
                }
            ]
        }
        
    },
    methods: {
        /**
         * Toggles the display this section of the resume.
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