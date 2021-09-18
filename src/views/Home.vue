<template>
  <div>
    <TheJumbotron />
    <about-me/>
    <work-exp id="we"/>
    <edu-exp id="edu"/>
    <my-skills id="skills"/>
  </div>
</template>

<script>
  import TheJumbotron from '../components/TheJumbotron'
  import AboutMe from '../components/AboutMe'
  import WorkExp from '../components/WorkExp'
  import EduExp from '../components/EduExp'
  import MySkills from '../components/MySkills'

  export default {
    name: 'Home',

    components: {
      TheJumbotron,
      AboutMe,
      WorkExp,
      EduExp,
      MySkills,
    },
  }
</script>
