<template>
   <div style="text-align:center; margin-top:30px"> 
                        <div v-if="!StyperInputDisable && !Styperpass1 && !deficultyselected">
                          <h1>:::SpeedCalculas:::</h1> 
                          <h2>SELECT GAME DEFICULTY</h2>
                          <br><br>  
                            <div class="startbtn" v-on:click="easy()">
                              Easy
                            </div><br><br><br>
                            <div class="startbtn" v-on:click="medium()">
                              Medium
                            </div><br><br><br>
                            <div class="startbtn" v-on:click="hard()">
                              Hard
                            </div>
                        </div>
                        <div v-if="!StyperInputDisable && !cStyperpass1 && deficultyselected">
                            <h1>{{CalculasQue[0]}}</h1>
                            <input v-on:keyup="ccheck()" type="text" autofocus v-model="cStyperInput" style="text-align:center; margin-top:30px; font-size: 20px ;"  /><br>
                            <b>(1/3) Remaining Time: {{timerCount}}</b>
                        </div>
                        <div v-if="(!StyperInputDisable && cStyperpass1) && !cStyperpass2">
                            <h1>{{CalculasQue[1]}}</h1>
                            <input v-on:keyup="ccheck1()" v-model="cStyperInput" style="text-align:center; margin-top:30px; font-size: 20px ;"  /><br>
                            <b>(2/3) Remaining Time: {{timerCount}}</b>
                        </div> 
                        <div v-if="(!StyperInputDisable && cStyperpass1 && cStyperpass2) && !cStyperpass3">
                            <h1>{{CalculasQue[2]}}</h1>
                            <input v-on:keyup="ccheck2()" v-model="cStyperInput" style="text-align:center; margin-top:30px; font-size: 20px ;"  /><br>
                            <b>(3/3) Remaining Time: {{timerCount}}</b>
                        </div>
                        <div v-if="over && StyperInputDisable"> 
                            <img v-bind:src="require('../assets/images/giphy.gif')"  style="width:15% ;"><br>
                            <b>You failed to pass the test</b><br><br><br> 
                            <div class="startbtn" v-on:click="retry()">
                              Re-Try
                            </div>
                        </div>
                        <div v-if="welldone && StyperInputDisable"> 
                            <img v-bind:src="require('../assets/images/200w.gif')"  style="width:15% ;"><br>
                            <b>You pass the Speed-Typer Test<br>In {{mode}} Mode {{trymode}}</b><br><br><br> 
                            <div class="startbtn" v-on:click="retry()">
                              Re-Try
                            </div>
                        </div> 
                    </div>
</template>

<script>
export default {
  name: 'FastType',
   data(){
                    return{ 
                        CalculasQue:['(12/4)*3','10000/100','(8*8)/32'],
                        StyperInput: "",
                        cStyperInput: "",
                        StyperWords:['Elephant','Azazel','Mazzard'], 
                        StyperInputDisable: false,
                        timerEnabled: true, 
                        timerCount: 0, 
                        Styperpass1:false,
                        Styperpass2:false,
                        Styperpass3:false,
                        cStyperpass1:false,
                        cStyperpass2:false,
                        cStyperpass3:false,
                        over:false,
                        welldone:false,   
                        deficultyselected:false,
                        mode:"" ,
                        trymode:""
                    }
                },
                methods:{ 
                    retry(){
                            location.reload(); 
                    }, 
                    pause() {
                        this.timerEnabled = false;
                    },
                    check(){
                        console.log(this.StyperWords[0],this.StyperInput)
                        if(this.StyperInput==this.StyperWords[0]){
                            console.log(this.StyperWords[0],this.StyperInput)  
                            this.Styperpass1 = true;
                            this.StyperInput = "";  
                        }  
                    },
                    check1(){ 
                      console.log(this.StyperWords[1],this.StyperInput) 
                        if(this.StyperInput==this.StyperWords[1]){ 
                            this.Styperpass2 = true;
                            this.StyperInput = ""; 
                        }
                    },
                    check2(){ 
                      console.log(this.StyperWords[2],this.StyperInput)
                        if(this.StyperInput==this.StyperWords[2]){ 
                            this.Styperpass3 = true;
                            this.StyperInput = "";
                            this.timerEnabled = false; 
                            this.won();
                        }
                    }, 
                    gameover(){
                        this.StyperInputDisable=true;
                        this.timerEnabled= false;
                        this.timerCount= 12;
                        this.Styperpass1=false;
                        this.Styperpass2=false;
                        this.Styperpass3=false; 
                        this.cStyperpass1=false;
                        this.cStyperpass2=false;
                        this.csStyperpass3=false; 
                        this.over=true;
                        this.deficultyselected=false;
                    },
                    won(){
                        this.StyperInputDisable=true;
                        this.timerEnabled= false;
                        this.timerCount= 12;
                        this.Styperpass1=false;
                        this.Styperpass2=false;
                        this.Styperpass3=false; 
                        this.cStyperpass1=false;
                        this.cStyperpass2=false;
                        this.cStyperpass3=false; 
                        this.welldone=true;
                        this.deficultyselected=false;
                        console.log("WON")
                    },
                    easy(){
                        this.timerCount= 30;
                        this.CalculasQue=['(12/4)*3','10000/100','(8*8)/32'];
                        this.deficultyselected=true; 
                        this.mode = "Easy"
                        this.trymode = "try Medium or Hard Modes"
                    },
                    medium(){
                      this.timerCount= 20;
                      this.CalculasQue=['(16/4)*(120/60)','11200/100','((80-10)/7)*10'];
                      this.deficultyselected=true; 
                      this.mode = "Medium"
                      this.trymode = "try Hard Mode"
                    },
                    hard(){
                      this.timerCount= 20;
                      this.CalculasQue=['((12+12)/6)*(13-9)','1.12*1000','(80*8)/32'];
                      this.deficultyselected=true;
                      this.mode = "Hard"
                      this.trymode = ". Good Luck Calc!"
                    },
                    ccheck(){
                         console.log("ccheck",this.mode)
                         if(this.mode=="Easy"){
                          console.log("easy")
                            if(this.cStyperInput==9){  
                            this.cStyperpass1 = true;
                            this.cStyperInput = "";  
                            }  
                         }
                         if(this.mode=="Medium"){
                          console.log("medium")
                            if(this.cStyperInput==8){  
                            this.cStyperpass1 = true;
                            this.cStyperInput = "";  
                            }  
                         }
                         if(this.mode=="Hard"){
                          console.log("hard")
                            if(this.cStyperInput==16){  
                            this.cStyperpass1 = true;
                            this.cStyperInput = "";  
                            }  
                         }
                        
                    },
                    ccheck1(){
                        console.log("ccheck1")
                        
                        if(this.mode=="Easy"){
                          console.log("easy")
                            if(this.cStyperInput==100){   
                            this.cStyperpass2 = true;
                            this.cStyperInput = ""; 
                          }
                         }
                         if(this.mode=="Medium"){
                          console.log("medium")
                            if(this.cStyperInput==112){   
                            this.cStyperpass2 = true;
                            this.cStyperInput = ""; 
                          }
                         }
                         if(this.mode=="Hard"){
                          console.log("hard")
                            if(this.cStyperInput==1120){   
                            this.cStyperpass2 = true;
                            this.cStyperInput = ""; 
                          }
                         }
                    },
                    ccheck2(){
                        console.log("ccheck2")
                        


                        if(this.mode=="Easy"){
                          console.log("easy")
                            if(this.cStyperInput==2){  
                            this.cStyperpass3 = true;
                            this.over=false;
                            this.cStyperInput = "";
                            this.timerEnabled = false; 
                            this.won();
                            }
                         }
                         if(this.mode=="Medium"){
                          console.log("medium")
                            if(this.cStyperInput==100){  
                            this.cStyperpass3 = true;
                            this.over=false;
                            this.cStyperInput = "";
                            this.timerEnabled = false; 
                            this.won();
                            }
                         }
                         if(this.mode=="Hard"){
                          console.log("hard")
                            if(this.cStyperInput==20){  
                            this.cStyperpass3 = true;
                            this.over=false;
                            this.cStyperInput = "";
                            this.timerEnabled = false; 
                            this.won();
                            }
                         }


                    },
                     
                },
                watch: { 
                    timerEnabled(value) {
                        if (value) {
                            setTimeout(() => {
                                this.timerCount--; 
                            }, 1000);
                        }
                    }, 
                    timerCount: {
                        handler(value) { 
                            if (value > 0 && this.timerEnabled) {
                                setTimeout(() => {
                                    this.timerCount--; 
                                    if(this.timerCount==0){
                                        this.gameover()
                                    }
                                }, 1000);
                            } 
                        },
                        immediate: true // This ensures the watcher is triggered upon creation
                    } 
                    }   
            
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.startbtn{
 text-align: center;
 color:white;
 width:20%;
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
 width:20%;
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
