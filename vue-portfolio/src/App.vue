<template>
  <div id="app">
    <Navbar @ChangePage="ChangePage"/>

    <div style="width: 70%, textAlign: center">
        <div class="Page">
          <Page :title="pageInfos[currentIndex].title" :subtitle="pageInfos[currentIndex].subtitle"/>
          <p>Hey there! My name is Gabriel Lucena, also known as FR4CT1ONS.</p>
          <p>I am an aspiring game programmer, artist and designer. Currently, I'm graduating in Information Technology at Universidade Federal do Rio Grande do Norte. 
              Over there, I'm primarily studying game development and design along with software engineering. I am also studying arts as an auto-didact. 
              After I graduate in I.T., I plan to stock up on money for taking a bachelor's degree course in arts/game arts.</p>
          <p>I have already worked on multiple games with two W.I.P small projects already published on GameJolt and itch.io - Poço Frio and Single Fighter - and am developing a personal project more privately.</p>
          <p>I have experience with C/C++, C# and with the Unity game engine. Currently, I'm studying the Unreal engine.</p>
          <p>When it comes to arts, I have experience in 2D concept and final art, as well as 3D modelling in general. Currently, I'm studying animation.</p>
          <br/>
          <p>Right now, the public project I'm giving most of my attention to is Single Fighter. Go check it out! <a href="https://fr4ct1ons.itch.io/single-fighter">https://fr4ct1ons.itch.io/single-fighter</a></p>
        </div>
        <ContactForm/>
      </div>
  </div>
</template>

<script>
import Navbar from "./Navbar.vue"
import Page from "./Page.vue"
import ContactForm from "./ContactForm.vue"

export default {
  name: 'App',
  created()
  {
    this.currentIndex = 1;
  },
  components: {
    Navbar,
    Page,
    ContactForm
  },
  methods: {
    ChangePage(index )
    {
      this.currentIndex = index;
      //alert(this.pageInfos[this.currentIndex].title);
    }
  },
  data: () => ({
    currentIndex : 1,
    pageInfos: 
  [
    {
      title: "ART GALLERY", subtitle: "My works of art"
    },
    {
      title: "WHO AM I", subtitle: "Introducing who I am, what I work with and my goals"
    },
    {
      title: "GAMES", subtitle: "Games I worked on"
    },
    {
      title: "SOFTWARE", subtitle: "Software I worked on"
    }
  ]
  })
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: 0%;
  /*margin-top: 60px;*/
}

body{
  margin: 0%;
  background-color: black;
}

.Page
{
  width: 66%;
  margin: auto;
  display: block
}

.Page h1
{
  color: red;
}

.Page h2
{
  color: rgb(150, 150, 150)
}
.Page p
{
  color: white;
}
</style>
