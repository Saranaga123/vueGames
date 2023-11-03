<template>
   <div style="text-align:center; margin-top:30px"> 
                        <div v-if="!StyperInputDisable && !Styperpass1 && !deficultyselected">
                          <h1>:::Find The Bombs:::</h1> 
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
                        <div v-if="!StyperInputDisable && deficultyselected">
                             <div>
                                <button class="ftmbtn" 	v-on:click="	ftmbtn1()	"	>	<b>{{	ftm1	}}</b></button>
                                <button class="ftmbtn" 	v-on:click="	ftmbtn2()	"	>	<b>{{	ftm2	}}</b></button>
                                <button class="ftmbtn" 	v-on:click="	ftmbtn3()	"	>	<b>{{	ftm3	}}</b></button>
                                <button class="ftmbtn" 	v-on:click="	ftmbtn4()	"	>	<b>{{	ftm4	}}</b></button>
                                <button class="ftmbtn" 	v-on:click="	ftmbtn5()	"	>	<b>{{	ftm5	}}</b></button>
                                <button class="ftmbtn" 	v-on:click="	ftmbtn6()	"	>	<b>{{	ftm6	}}</b></button>
                                <button class="ftmbtn" 	v-on:click="	ftmbtn7()	"	>	<b>{{	ftm7	}}</b></button>
                                <button class="ftmbtn" 	v-on:click="	ftmbtn8()	"	>	<b>{{	ftm8	}}</b></button>
                                <button class="ftmbtn" 	v-on:click="	ftmbtn9()	"	>	<b>{{	ftm9	}}</b></button>
                                <button class="ftmbtn" 	v-on:click="	ftmbtn10()	"	>	<b>{{	ftm10	}}</b></button>
                                <br>
                                <button class="ftmbtn" 	v-on:click="	ftmbtn11()	"	>	<b>{{	ftm11	}}</b></button>
                                <button class="ftmbtn" 	v-on:click="	ftmbtn12()	"	>	<b>{{	ftm12	}}</b></button>
                                <button class="ftmbtn" 	v-on:click="	ftmbtn13()	"	>	<b>{{	ftm13	}}</b></button>
                                <button class="ftmbtn" 	v-on:click="	ftmbtn14()	"	>	<b>{{	ftm14	}}</b></button>
                                <button class="ftmbtn" 	v-on:click="	ftmbtn15()	"	>	<b>{{	ftm15	}}</b></button>
                                <button class="ftmbtn" 	v-on:click="	ftmbtn16()	"	>	<b>{{	ftm16	}}</b></button>
                                <button class="ftmbtn" 	v-on:click="	ftmbtn17()	"	>	<b>{{	ftm17	}}</b></button>
                                <button class="ftmbtn" 	v-on:click="	ftmbtn18()	"	>	<b>{{	ftm18	}}</b></button>
                                <button class="ftmbtn" 	v-on:click="	ftmbtn19()	"	>	<b>{{	ftm19	}}</b></button>
                                <button class="ftmbtn" 	v-on:click="	ftmbtn20()	"	>	<b>{{	ftm20	}}</b></button>
                                <br>
                                <button class="ftmbtn" 	v-on:click="	ftmbtn21()	"	>	<b>{{	ftm21	}}</b></button>
                                <button class="ftmbtn" 	v-on:click="	ftmbtn22()	"	>	<b>{{	ftm22	}}</b></button>
                                <button class="ftmbtn" 	v-on:click="	ftmbtn23()	"	>	<b>{{	ftm23	}}</b></button>
                                <button class="ftmbtn" 	v-on:click="	ftmbtn24()	"	>	<b>{{	ftm24	}}</b></button>
                                <button class="ftmbtn" 	v-on:click="	ftmbtn25()	"	>	<b>{{	ftm25	}}</b></button>
                                <button class="ftmbtn" 	v-on:click="	ftmbtn26()	"	>	<b>{{	ftm26	}}</b></button>
                                <button class="ftmbtn" 	v-on:click="	ftmbtn27()	"	>	<b>{{	ftm27	}}</b></button>
                                <button class="ftmbtn" 	v-on:click="	ftmbtn28()	"	>	<b>{{	ftm28	}}</b></button>
                                <button class="ftmbtn" 	v-on:click="	ftmbtn29()	"	>	<b>{{	ftm29	}}</b></button>
                                <button class="ftmbtn" 	v-on:click="	ftmbtn30()	"	>	<b>{{	ftm30	}}</b></button>
                                <br>
                                <button class="ftmbtn" 	v-on:click="	ftmbtn31()	"	>	<b>{{	ftm31	}}</b></button>
                                <button class="ftmbtn" 	v-on:click="	ftmbtn32()	"	>	<b>{{	ftm32	}}</b></button>
                                <button class="ftmbtn" 	v-on:click="	ftmbtn33()	"	>	<b>{{	ftm33	}}</b></button>
                                <button class="ftmbtn" 	v-on:click="	ftmbtn34()	"	>	<b>{{	ftm34	}}</b></button>
                                <button class="ftmbtn" 	v-on:click="	ftmbtn35()	"	>	<b>{{	ftm35	}}</b></button>
                                <button class="ftmbtn" 	v-on:click="	ftmbtn36()	"	>	<b>{{	ftm36	}}</b></button>
                                <button class="ftmbtn" 	v-on:click="	ftmbtn37()	"	>	<b>{{	ftm37	}}</b></button>
                                <button class="ftmbtn" 	v-on:click="	ftmbtn38()	"	>	<b>{{	ftm38	}}</b></button>
                                <button class="ftmbtn" 	v-on:click="	ftmbtn39()	"	>	<b>{{	ftm39	}}</b></button>
                                <button class="ftmbtn" 	v-on:click="	ftmbtn40()	"	>	<b>{{	ftm40	}}</b></button>
                                <br>
                                <button class="ftmbtn" 	v-on:click="	ftmbtn41()	"	>	<b>{{	ftm41	}}</b></button>
                                <button class="ftmbtn" 	v-on:click="	ftmbtn42()	"	>	<b>{{	ftm42	}}</b></button>
                                <button class="ftmbtn" 	v-on:click="	ftmbtn43()	"	>	<b>{{	ftm43	}}</b></button>
                                <button class="ftmbtn" 	v-on:click="	ftmbtn44()	"	>	<b>{{	ftm44	}}</b></button>
                                <button class="ftmbtn" 	v-on:click="	ftmbtn45()	"	>	<b>{{	ftm45	}}</b></button>
                                <button class="ftmbtn" 	v-on:click="	ftmbtn46()	"	>	<b>{{	ftm46	}}</b></button>
                                <button class="ftmbtn" 	v-on:click="	ftmbtn47()	"	>	<b>{{	ftm47	}}</b></button>
                                <button class="ftmbtn" 	v-on:click="	ftmbtn48()	"	>	<b>{{	ftm48	}}</b></button>
                                <button class="ftmbtn" 	v-on:click="	ftmbtn49()	"	>	<b>{{	ftm49	}}</b></button>
                                <button class="ftmbtn" 	v-on:click="	ftmbtn50()	"	>	<b>{{	ftm50	}}</b></button>

                             </div>
                             
                            <b>Remaining Time: {{timerCount}}</b>
                        </div> 
                        <div v-if="over && StyperInputDisable"> 
                            <img v-bind:src="require('../assets/images/giphy.gif')"  style="width:15% ;"><br>
                            <b>You failed to find 2 bombs</b><br><br><br> 
                            <div class="startbtn" v-on:click="retry()">
                              Re-Try
                            </div>
                        </div>
                        <div v-if="welldone && StyperInputDisable"> 
                            <img v-bind:src="require('../assets/images/200w.gif')"  style="width:15% ;"><br>
                            <b>You pass the Test<br>In {{mode}} Mode {{trymode}}</b><br><br><br> 
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
                        trymode:"",
                        mine1:false,
                        mine2:false,

                        ftm1:" ",
                        ftm2:" ",
                        ftm3:" ",
                        ftm4:" ",
                        ftm5:" ",
                        ftm6:" ",
                        ftm7:" ",
                        ftm8:" ",
                        ftm9:" ",
                        ftm10:" ", 
                        ftm11:" ",
                        ftm12:" ",
                        ftm13:" ",
                        ftm14:" ",
                        ftm15:" ",
                        ftm16:" ",
                        ftm17:" ",
                        ftm18:" ",
                        ftm19:" ",
                        ftm20:" ",
                        ftm21:" ",
                        ftm22:" ",
                        ftm23:" ",
                        ftm24:" ",
                        ftm25:" ",
                        ftm26:" ",
                        ftm27:" ",
                        ftm28:" ",
                        ftm29:" ",
                        ftm30:" ",
                        ftm31:" ",
                        ftm32:" ",
                        ftm33:" ",
                        ftm34:" ",
                        ftm35:" ",
                        ftm36:" ",
                        ftm37:" ",
                        ftm38:" ",
                        ftm39:" ",
                        ftm40:" ",
                        ftm41:" ",
                        ftm42:" ",
                        ftm43:" ",
                        ftm44:" ",
                        ftm45:" ",
                        ftm46:" ",
                        ftm47:" ",
                        ftm48:" ",
                        ftm49:" ",
                        ftm50:" ", 
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
                        this.deficultyselected=true; 
                        this.mode = "Easy"
                        this.trymode = "try Medium or Hard Modes"
                    },
                    medium(){
                      this.timerCount= 20;
                      this.deficultyselected=true; 
                      this.mode = "Medium"
                      this.trymode = "try Hard Mode"
                    },
                    hard(){
                      this.timerCount= 12;
                      this.deficultyselected=true;
                      this.mode = "Hard"
                      this.trymode = ". Good Luck !"
                    },
                    ftmbtn1	(){	this.	ftm1	="☺"	},
                    ftmbtn2	(){	if(this.mode=="Hard"){
                                    this.	ftm2	="╬";
                                    this.mine1=true;
                                    if(this.mine2==true){
                                        this.won() 
                                    }}else{
                                        this.	ftm2	="☺";
                                    } 	},
                    ftmbtn3	(){	this.	ftm3	="☺"	},
                    ftmbtn4	(){	this.	ftm4	="☺"	},
                    ftmbtn5	(){	this.	ftm5	="☺"	},
                    ftmbtn6	(){	this.	ftm6	="☺"	},
                    ftmbtn7	(){	this.	ftm7	="☺"	},
                    ftmbtn8	(){	this.	ftm8	="☺"	},
                    ftmbtn9	(){	this.	ftm9	="☺"	},
                    ftmbtn10	(){	this.	ftm10	="☺"	},
                    ftmbtn11	(){	this.	ftm11	="☺"	},
                    ftmbtn12	(){	this.	ftm12	="☺"	},
                    ftmbtn13	(){	this.	ftm13	="☺"	},
                    ftmbtn14	(){	this.	ftm14	="☺"	},
                    ftmbtn15	(){	this.	ftm15	="☺"	},
                    ftmbtn16	(){	this.	ftm16	="☺"	},
                    ftmbtn17	(){	this.	ftm17	="☺"	},
                    ftmbtn18	(){	this.	ftm18	="☺"	},
                    ftmbtn19	(){	this.	ftm19	="☺"	},
                    ftmbtn20	(){	if(this.mode=="Easy"){
                                    this.	ftm20	="╬";
                                    this.mine1=true;
                                    if(this.mine2==true){
                                        this.won() 
                                    }}else{
                                        this.	ftm20	="☺";
                                    } 
                                    
                               },
                    ftmbtn21	(){	this.	ftm21	="☺"	},
                    ftmbtn22	(){	this.	ftm22	="☺"	},
                    ftmbtn23	(){	this.	ftm23	="☺"	},
                    ftmbtn24	(){	this.	ftm24	="☺"	},
                    ftmbtn25	(){	this.	ftm25	="☺"	},
                    ftmbtn26	(){	this.	ftm26	="☺"	},
                    ftmbtn27	(){	
                        if(this.mode=="Medium"){
                                    this.	ftm27	="╬";
                                    this.mine1=true;
                                    if(this.mine2==true){
                                        this.won() 
                                    }}else{
                                        this.	ftm27	="☺";
                                    } },
                    ftmbtn28	(){	this.	ftm28	="☺"	},
                    ftmbtn29	(){	this.	ftm29	="☺"	},
                    ftmbtn30	(){	this.	ftm30	="☺"	},
                    ftmbtn31	(){	this.	ftm31	="☺"	},
                    ftmbtn32	(){	if(this.mode=="Hard"){
                                    this.	ftm32	="╬";
                                    this.mine2=true;
                                    if(this.mine1==true){
                                        this.won() 
                                    }}else{
                                        this.	ftm32	="☺";
                                    } },
                    ftmbtn33	(){	this.	ftm33	="☺"	},
                    ftmbtn34	(){	this.	ftm34	="☺"	},
                    ftmbtn35	(){	
                                    if(this.mode=="Easy"){
                                    this.	ftm35	="╬";
                                    this.mine2=true;
                                    if(this.mine1==true){
                                        this.won() 
                                    }else{
                                       this.	ftm35	="☺"; 
                                    }
                                    }
                         },
                    ftmbtn36	(){	this.	ftm36	="☺"	},
                    ftmbtn37	(){	this.	ftm37	="☺"	},
                    ftmbtn38	(){	this.	ftm38	="☺"	},
                    ftmbtn39	(){	this.	ftm39	="☺"	},
                    ftmbtn40	(){	this.	ftm40	="☺"	},
                    ftmbtn41	(){	this.	ftm41	="☺"	},
                    ftmbtn42	(){	this.	ftm42	="☺"	},
                    ftmbtn43	(){	this.	ftm43	="☺"	},
                    ftmbtn44	(){	this.	ftm44	="☺"	},
                    ftmbtn45	(){	this.	ftm45	="☺"	},
                    ftmbtn46	(){	this.	ftm46	="☺"	},
                    ftmbtn47	(){	this.	ftm47	="☺"	},
                    ftmbtn48	(){	this.	ftm48	="☺"	},
                    ftmbtn49	(){	if(this.mode=="Medium"){
                                    this.	ftm49	="╬";
                                    this.mine2=true;
                                    if(this.mine1==true){
                                        this.won() 
                                    }}else{
                                        this.	ftm49	="☺";
                                    } },
                    ftmbtn50	(){	this.	ftm50	="☺"	}
                     
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
.ftmbtn{
                max-width: 50px;
                min-width: 50px;
                max-height: 50px;
                min-height: 50px;
                font-size: 30px;
                color:white;
                font-weight: bold;
                background-image: linear-gradient(#34966aa2,#34966a,#34966ac0, #34966aab);
             }
 
</style>
