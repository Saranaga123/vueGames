<template>
  <nav>
    <router-link to="/" class="naviLinks">Home</router-link> &nbsp;&nbsp; || 
    <router-link to="/FastTyper">FastTyper</router-link> | 
    <router-link to="/FTBombs">FTBombs</router-link> | 
    <router-link to="/TicTacToe">TicTacToe</router-link> | 
    <router-link to="/SpeedCalc">SpeedCalc </router-link> || &nbsp;&nbsp;
    <router-link to="/about">About</router-link> 
  </nav>
   
     <router-view/>
        <div class="ftr">
          <img v-bind:src="require('./assets/images/6.gif')" style="max-height:75px;float:left;position:fixed;bottom:0;left:0"/>
          <span style="float:left; margin-left:150px">Created By Asitha Saranga Dissanayaka<br>
          <span style="font-size:12px">EDUONIX Vue Game Collection</span></span></div>
 
</template>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  width:100%;
  position: fixed;
  top:0px;
  left:0px;
  padding: 30px; 
  background-image: linear-gradient(rgba(255, 255, 255, 0.89),rgba(255, 255, 255, 0.774),rgba(255, 255, 255, 0.521), rgba(255, 255, 255, 0.11));

  a {
    font-weight: bold;
    color: #2c3e50;
    text-decoration: none;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
  a:hover {
    font-weight: bold;
    color: #42b983;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
.ftr{
  width:100%;
  position:fixed;
  font-weight: bold;
  text-align: left;
  bottom:0px;
  color: #2c3e50;
  left:0px;
  padding: 5px; 
  max-height: 50px;
  min-height: 50px;
  background-image: linear-gradient(rgba(255, 255, 255, 0.11),rgba(255, 255, 255, 0.274),rgba(255, 255, 255, 0.377), rgba(255, 255, 255, 0.5));
}

 
</style>
