<template>
    <div class="main">
        <div id="about-me">
            <h1>{{name}}</h1>
            <img id ="headshot" src="../assets/hs1.jpg" alt="A photo of me!">
            <p id="summary">{{summary}}</p>
        </div>
        <div id="display-container">
            <education></education>
            <projects></projects>
            <skills></skills>
            <experience></experience>
        </div>
    </div>
</template>

<script>
import Education from './Education.vue'
import Projects from './Projects.vue'
import Skills from './Skills.vue'
import Experience from './Experience.vue'

export default {
    name: "resume",
    components: {
        Education,
        Projects,
        Skills,
        Experience
    },
    data() {
        return {
            name: "John Freund",
            summary: "Effective communicator and critical thinker. Former sales  representative seeking a career in software development, looking to  apply my past experience and passion for helping others improve their  lives, while expanding my skill set as a programmer. ",
            
        }
    }
}
</script>

<style>
h1 {
    text-align: left;
    color:darkblue;
}
#summary {
    text-align: left;
    width: 45%;
}
h2 {
    border:darkblue solid 5px;
    border-radius: 5px;
    cursor: help;
    padding: 2px 10px 2px 10px;
}
h2:hover{
    color: royalblue;
    border: royalblue solid 5px;
}
#headers {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
}
#about-me {
    display: flex;
    flex-direction: column
}
#headshot {
    width: 256px;
    height: auto;
    border-radius: 50%;
}
#display-container {
    display: flex;
    flex-direction: row;
    justify-content: space-evenly;
}
</style>
