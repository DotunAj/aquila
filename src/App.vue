<template>
  <div class="container">
    <Loading v-if="loading"/>
    <Menu v-if="data.social_media" :links="data.social_media" :menuOpened="showClose"/>
    <div class="hamburger" :class="{ close: showClose }" @click="openMenu">
    </div>
    <div class="content">
      <socials v-if="data.social_media" :links="data.social_media"/>
      <h1>{{data.name}}</h1>
      <img class="cover-photo" src="./assets/lady.png">
      <navigation/>
    </div>
  </div>
</template>

<script>
import Menu from './components/Menu.vue'
import Navigation from './components/Navigation.vue'
import Socials from './components/Socials.vue'
import Loading from './components/Loading.vue'
import axios from 'axios'

export default {
  name: 'App',
  components: {
    Navigation,
    Socials,
    Menu,
    Loading
  },

  data(){
    return{
      showClose: false,
      loading: true,
      data: {}
    }
  },
  methods:{
    openMenu(){
      this.showClose = !this.showClose
    }
  },

  async created(){
    const response = await axios.get('https://hirng-x2021.glitch.me/api');
    this.loading = false;
    this.data = response.data;
  } 
}
</script>

<style>
*{
  margin: 0;
  padding: 0;
}

body, html{
  color: #fff;
  font-family: 'Roboto', sans-serif;
}

#app{
  background: rgb(22, 21, 21);
}

.container{
  position: relative;
  display: flex;
  background-color:#CB2964;
  height: 100%;
}

.container::after{
  content: '';
  position: absolute;
  top:0;
  width: 50%;
  height: 100%;
  background-color:#BD0F4D;
  z-index: 1;
}

.content{
  position: relative;
  width: 100%;
  height: 100vh;
  z-index: 2;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.content h1{
  font-weight: lighter;
  font-size: 34px;
  letter-spacing: 19px;
  text-align: center;
}

.cover-photo{
  height: 550px;
  margin: 60px 0;
  box-shadow: 0px 4px 85px 5px rgba(0, 0, 0, 0.25);
  transition-duration: 0.5s;
}

.cover-photo:hover{
  box-shadow: 0px 4px 85px 5px rgba(0, 0, 0, 0.45);
}

@media only screen and (min-width: 1440px) {
  .container{
    margin: auto;
  }
}

@media only screen and (max-width: 750px) {
  .cover-photo{
    height: 400px;
  }
}

@media only screen and (max-width: 500px) {
  .content{
    height: 100vh;
    justify-content: flex-start;  
  }
  .content h1{
    font-weight: lighter;
    margin-top: 100px;
    font-size: 30px;
    letter-spacing: 19px;
  }

  .cover-photo{
    height: 250px;
  }

  .hamburger {
    position: fixed;
    top: 35px;
    left: calc(50% - 15px);
    width: 30px;
    cursor: pointer;
    z-index: 100;
    margin-bottom: 50px;
  }

  .hamburger::after,
  .hamburger::before {
    background-color: #fff;
    border-radius: 3px;
    content: '';
    display: block;
    height: 2px;
    margin: 5px 0;
    transition: all 0.6s ease-in-out;
  }

  .close {
    display: block;
  }

  .close:before {
    background-color: #fff;
    transform: translateY(3.5px) rotate(135deg);
  }

  .close:after {
    background-color: #fff;
    transform: translateY(-3.5px) rotate(-135deg);
  }
    
}
</style>
