<template>
  <div class="wrapper"> 
    <h2>Game List</h2>
    <div class = "row">
        <div class="col-3">  
          FastTyper
          <img v-bind:src="require('../assets/images/typer.png')" style="width:100%;margin-top:20px"/>
          <p style="color:#379c6f">
              Player can select deficulty level.<br><br>
              Player have to type given words within time limit to win.
          </p>
          <router-link to="/FastTyper" class="naviLinks">
          <div class="startbtn">
            Start
          </div>
          </router-link>
        </div>
        <div class="col-3"> 
          Find The Bombs 
          <img v-bind:src="require('../assets/images/bomb.png')" style="width:100%;margin-top:20px"/>
          <p style="color:#379c6f">
              Player can select deficulty level.<br><br>
              Player have to find 2 hidden mines from the grid within time.
          </p>
          <router-link to="/FTBombs" class="naviLinks">
          <div class="startbtn">
            Start
          </div>
          </router-link>
        </div>
        <div class="col-3"> 
          Tic Tac Toe
          <img v-bind:src="require('../assets/images/tic.png')" style="width:100%;margin-top:20px"/>
          <p style="color:#379c6f"> 
              TIC TAC TOE !<br><br>
              No Rules, Just take your turn.<br><br>
          </p>
          <router-link to="/TicTacToe" class="naviLinks">
          <div class="startbtn">
            Start
          </div>
          </router-link>
        </div>
        <div class="col-3"> 
          SpeedCalc
          <img v-bind:src="require('../assets/images/calc.png')" style="width:100%;margin-top:20px"/>
          <p style="color:#379c6f">
              Player can select deficulty level.<br><br>
              Player have to solve the given math questions within time limit to win.
          </p>
          <router-link to="/SpeedCalc" class="naviLinks">
          <div class="startbtn">
            Start
          </div>
          </router-link>
        </div>
         
    </div>
  </div>
</template> 
<script> 
export default {
  name: 'HomeView'
  }  
    
</script>
<style scoped>
.wrapper{
  text-align: left;
  padding: 10px;
  color: #2b7c58;
}
.row{
  width:100%;
  color: #2b7c58;
  font-weight: bold;
}
.col-3{
  width: 30%;
  text-align: center;
  min-height:50vh;
  padding: 10px;
  float: left;
  background-color: rgba(255, 255, 255, 0.562);
  margin: 1px;
  margin-bottom: 5px;
}
.col-3:hover{
  width: 30%;
  text-align: center;
  min-height:50vh;
  padding: 10px;
  float: left;
  background-color: rgba(255, 255, 255, 0.89);
  margin: 1px;
  margin-bottom: 5px;
}
.startbtn{
 text-align: center;
 color:white;
 width:55%;
 border-radius: 5px;
 min-height: 0px;
 padding: 10px 5px; 
  text-decoration: none;
  display: inline-block;
 background-color: #2b7c58;
}
.startbtn:hover{
 text-align: center;
 color:white;
 width:55%;
 border-radius: 5px;
 min-height: 0px;
 padding: 10px 5px; 
  text-decoration: none;
  display: inline-block;
 background-color: #34966a;
 cursor: pointer;
 box-shadow: 1px 1px 5px 3px #ccc;
}

</style>
 
