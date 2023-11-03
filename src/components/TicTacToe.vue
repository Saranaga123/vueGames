<template>
   <div style="text-align:center; margin-top:30px"> 
                         
                        <div v-if="!StyperInputDisable ">
                            <h3>Player "X" Starts First</h3>
        <!-- 3*3 grid of Boxes -->
        <input type="text" id="b1" v-on:click=
            "myfunc_3(); myfunc();" readonly>
   
        <input type="text" id="b2" v-on:click=
            "myfunc_4(); myfunc();" readonly>
   
        <input type="text" id="b3" v-on:click=
            "myfunc_5(); myfunc();" readonly>
        <br> 
   
        <input type="text" id="b4" v-on:click=
            "myfunc_6(); myfunc();" readonly>
               
        <input type="text" id="b5" v-on:click=
            "myfunc_7(); myfunc();" readonly>
   
        <input type="text" id="b6" v-on:click=
            "myfunc_8(); myfunc();" readonly>
        <br> 
   
        <input type="text" id="b7" v-on:click=
            "myfunc_9(); myfunc();" readonly>
   
        <input type="text" id="b8" v-on:click=
            "myfunc_10();myfunc();" readonly>
   
        <input type="text" id="b9" v-on:click=
            "myfunc_11();myfunc();" readonly>
   
        <!-- Grid end here  -->
        <br><br> 
        <!-- Button to reset game -->
         
        <div id="but" class="startbtn" v-on:click="myfunc_2()">
                              Reset
                            </div>
   
        <br> 
        <!-- Space to show player turn -->
        <p id="print"></p> 
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
                        flag:1
                    }
                },
                methods:{ 
                     
                     myfunc() {
 
    // Setting DOM to all boxes or input field
    var b1, b2, b3, b4, b5, b6, b7, b8, b9;
    b1 = document.getElementById("b1").value;
    b2 = document.getElementById("b2").value;
    b3 = document.getElementById("b3").value;
    b4 = document.getElementById("b4").value;
    b5 = document.getElementById("b5").value;
    b6 = document.getElementById("b6").value;
    b7 = document.getElementById("b7").value;
    b8 = document.getElementById("b8").value;
    b9 = document.getElementById("b9").value;
 
    // Checking if Player X won or not and after
    // that disabled all the other fields
    if ((b1 == 'x' || b1 == 'X') && (b2 == 'x' ||
        b2 == 'X') && (b3 == 'x' || b3 == 'X')) {
        document.getElementById('print')
            .innerHTML = "Player X won";
        document.getElementById("b4").disabled = true;
        document.getElementById("b5").disabled = true;
        document.getElementById("b6").disabled = true;
        document.getElementById("b7").disabled = true;
        document.getElementById("b8").disabled = true;
        document.getElementById("b9").disabled = true;
        
    }
    else if ((b1 == 'x' || b1 == 'X') && (b4 == 'x' ||
        b4 == 'X') && (b7 == 'x' || b7 == 'X')) {
        document.getElementById('print')
            .innerHTML = "Player X won";
        document.getElementById("b2").disabled = true;
        document.getElementById("b3").disabled = true;
        document.getElementById("b5").disabled = true;
        document.getElementById("b6").disabled = true;
        document.getElementById("b8").disabled = true;
        document.getElementById("b9").disabled = true;
 
        
    }
    else if ((b7 == 'x' || b7 == 'X') && (b8 == 'x' ||
        b8 == 'X') && (b9 == 'x' || b9 == 'X')) {
        document.getElementById('print')
            .innerHTML = "Player X won";
        document.getElementById("b1").disabled = true;
        document.getElementById("b2").disabled = true;
        document.getElementById("b3").disabled = true;
        document.getElementById("b4").disabled = true;
        document.getElementById("b5").disabled = true;
        document.getElementById("b6").disabled = true;
        
    }
    else if ((b3 == 'x' || b3 == 'X') && (b6 == 'x' ||
        b6 == 'X') && (b9 == 'x' || b9 == 'X')) {
        document.getElementById('print')
            .innerHTML = "Player X won";
        document.getElementById("b1").disabled = true;
        document.getElementById("b2").disabled = true;
        document.getElementById("b4").disabled = true;
        document.getElementById("b5").disabled = true;
        document.getElementById("b7").disabled = true;
        document.getElementById("b8").disabled = true;
        
    }
    else if ((b1 == 'x' || b1 == 'X') && (b5 == 'x' ||
        b5 == 'X') && (b9 == 'x' || b9 == 'X')) {
        document.getElementById('print')
            .innerHTML = "Player X won";
        document.getElementById("b2").disabled = true;
        document.getElementById("b3").disabled = true;
        document.getElementById("b4").disabled = true;
        document.getElementById("b6").disabled = true;
        document.getElementById("b7").disabled = true;
        document.getElementById("b8").disabled = true;
        
    }
    else if ((b3 == 'x' || b3 == 'X') && (b5 == 'x' ||
        b5 == 'X') && (b7 == 'x' || b7 == 'X')) {
        document.getElementById('print')
            .innerHTML = "Player X won";
        document.getElementById("b1").disabled = true;
        document.getElementById("b2").disabled = true;
        document.getElementById("b4").disabled = true;
        document.getElementById("b6").disabled = true;
        document.getElementById("b8").disabled = true;
        document.getElementById("b9").disabled = true;
        
    }
    else if ((b2 == 'x' || b2 == 'X') && (b5 == 'x' ||
        b5 == 'X') && (b8 == 'x' || b8 == 'X')) {
        document.getElementById('print')
            .innerHTML = "Player X won";
        document.getElementById("b1").disabled = true;
        document.getElementById("b3").disabled = true;
        document.getElementById("b4").disabled = true;
        document.getElementById("b6").disabled = true;
        document.getElementById("b7").disabled = true;
        document.getElementById("b9").disabled = true;
        
    }
    else if ((b4 == 'x' || b4 == 'X') && (b5 == 'x' ||
        b5 == 'X') && (b6 == 'x' || b6 == 'X')) {
        document.getElementById('print')
            .innerHTML = "Player X won";
        document.getElementById("b1").disabled = true;
        document.getElementById("b2").disabled = true;
        document.getElementById("b3").disabled = true;
        document.getElementById("b7").disabled = true;
        document.getElementById("b8").disabled = true;
        document.getElementById("b9").disabled = true;
        
    }
 
    // Checking of Player X finish
    // Checking for Player 0 starts, Is player 0 won or
    // not and after that disabled all the other fields
    else if ((b1 == '0' || b1 == '0') && (b2 == '0' ||
        b2 == '0') && (b3 == '0' || b3 == '0')) {
        document.getElementById('print')
            .innerHTML = "Player 0 won";
        document.getElementById("b4").disabled = true;
        document.getElementById("b5").disabled = true;
        document.getElementById("b6").disabled = true;
        document.getElementById("b7").disabled = true;
        document.getElementById("b8").disabled = true;
        document.getElementById("b9").disabled = true;
        
    }
    else if ((b1 == '0' || b1 == '0') && (b4 == '0' ||
        b4 == '0') && (b7 == '0' || b7 == '0')) {
        document.getElementById('print')
            .innerHTML = "Player 0 won";
        document.getElementById("b2").disabled = true;
        document.getElementById("b3").disabled = true;
        document.getElementById("b5").disabled = true;
        document.getElementById("b6").disabled = true;
        document.getElementById("b8").disabled = true;
        document.getElementById("b9").disabled = true;
        
    }
    else if ((b7 == '0' || b7 == '0') && (b8 == '0' ||
        b8 == '0') && (b9 == '0' || b9 == '0')) {
        document.getElementById('print')
            .innerHTML = "Player 0 won";
        document.getElementById("b1").disabled = true;
        document.getElementById("b2").disabled = true;
        document.getElementById("b3").disabled = true;
        document.getElementById("b4").disabled = true;
        document.getElementById("b5").disabled = true;
        document.getElementById("b6").disabled = true;
        
    }
    else if ((b3 == '0' || b3 == '0') && (b6 == '0' ||
        b6 == '0') && (b9 == '0' || b9 == '0')) {
        document.getElementById('print')
            .innerHTML = "Player 0 won";
        document.getElementById("b1").disabled = true;
        document.getElementById("b2").disabled = true;
        document.getElementById("b4").disabled = true;
        document.getElementById("b5").disabled = true;
        document.getElementById("b7").disabled = true;
        document.getElementById("b8").disabled = true;
        
    }
    else if ((b1 == '0' || b1 == '0') && (b5 == '0' ||
        b5 == '0') && (b9 == '0' || b9 == '0')) {
        document.getElementById('print')
            .innerHTML = "Player 0 won";
        document.getElementById("b2").disabled = true;
        document.getElementById("b3").disabled = true;
        document.getElementById("b4").disabled = true;
        document.getElementById("b6").disabled = true;
        document.getElementById("b7").disabled = true;
        document.getElementById("b8").disabled = true;
        
    }
    else if ((b3 == '0' || b3 == '0') && (b5 == '0' ||
        b5 == '0') && (b7 == '0' || b7 == '0')) {
        document.getElementById('print')
            .innerHTML = "Player 0 won";
        document.getElementById("b1").disabled = true;
        document.getElementById("b2").disabled = true;
        document.getElementById("b4").disabled = true;
        document.getElementById("b6").disabled = true;
        document.getElementById("b8").disabled = true;
        document.getElementById("b9").disabled = true;
        
    }
    else if ((b2 == '0' || b2 == '0') && (b5 == '0' ||
        b5 == '0') && (b8 == '0' || b8 == '0')) {
        document.getElementById('print')
            .innerHTML = "Player 0 won";
        document.getElementById("b1").disabled = true;
        document.getElementById("b3").disabled = true;
        document.getElementById("b4").disabled = true;
        document.getElementById("b6").disabled = true;
        document.getElementById("b7").disabled = true;
        document.getElementById("b9").disabled = true;
        
    }
    else if ((b4 == '0' || b4 == '0') && (b5 == '0' ||
        b5 == '0') && (b6 == '0' || b6 == '0')) {
        document.getElementById('print')
            .innerHTML = "Player 0 won";
        document.getElementById("b1").disabled = true;
        document.getElementById("b2").disabled = true;
        document.getElementById("b3").disabled = true;
        document.getElementById("b7").disabled = true;
        document.getElementById("b8").disabled = true;
        document.getElementById("b9").disabled = true;
        
    }
 
    // Checking of Player 0 finish
    // Here, Checking about Tie
    else if ((b1 == 'X' || b1 == '0') && (b2 == 'X'
        || b2 == '0') && (b3 == 'X' || b3 == '0') &&
        (b4 == 'X' || b4 == '0') && (b5 == 'X' ||
        b5 == '0') && (b6 == 'X' || b6 == '0') &&
        (b7 == 'X' || b7 == '0') && (b8 == 'X' ||
        b8 == '0') && (b9 == 'X' || b9 == '0')) {
            document.getElementById('print')
                .innerHTML = "Match Tie";
             
    }
    else {
 
        // Here, Printing Result
        if (this.flag == 1) {
            document.getElementById('print')
                .innerHTML = "Player X Turn";
        }
        else {
            document.getElementById('print')
                .innerHTML = "Player 0 Turn";
        }
    }
},
myfunc_2() {
    location.reload();
    document.getElementById('b1').value = '';
    document.getElementById("b2").value = '';
    document.getElementById("b3").value = '';
    document.getElementById("b4").value = '';
    document.getElementById("b5").value = '';
    document.getElementById("b6").value = '';
    document.getElementById("b7").value = '';
    document.getElementById("b8").value = '';
    document.getElementById("b9").value = '';
 
},
myfunc_3() {
    if (this.flag == 1) {
        document.getElementById("b1").value = "X";
        document.getElementById("b1").disabled = true;
        this.flag = 0;
    }
    else {
        document.getElementById("b1").value = "0";
        document.getElementById("b1").disabled = true;
        this.flag = 1;
    }
},
myfunc_4() {
    if (this.flag == 1) {
        document.getElementById("b2").value = "X";
        document.getElementById("b2").disabled = true;
        this.flag = 0;
    }
    else {
        document.getElementById("b2").value = "0";
        document.getElementById("b2").disabled = true;
        this.flag = 1;
    }
},
 myfunc_5() {
    if (this.flag == 1) {
        document.getElementById("b3").value = "X";
        document.getElementById("b3").disabled = true;
        this.flag = 0;
    }
    else {
        document.getElementById("b3").value = "0";
        document.getElementById("b3").disabled = true;
        this.flag = 1;
    }
},
 
 myfunc_6() {
    if (this.flag == 1) {
        document.getElementById("b4").value = "X";
        document.getElementById("b4").disabled = true;
        this.flag = 0;
    }
    else {
        document.getElementById("b4").value = "0";
        document.getElementById("b4").disabled = true;
        this.flag = 1;
    }
},
 
 myfunc_7() {
    if (this.flag == 1) {
        document.getElementById("b5").value = "X";
        document.getElementById("b5").disabled = true;
        this.flag = 0;
    }
    else {
        document.getElementById("b5").value = "0";
        document.getElementById("b5").disabled = true;
        this.flag = 1;
    }
},
 
 myfunc_8() {
    if (this.flag == 1) {
        document.getElementById("b6").value = "X";
        document.getElementById("b6").disabled = true;
        this.flag = 0;
    }
    else {
        document.getElementById("b6").value = "0";
        document.getElementById("b6").disabled = true;
        this.flag = 1;
    }
},
 
 myfunc_9() {
    if (this.flag == 1) {
        document.getElementById("b7").value = "X";
        document.getElementById("b7").disabled = true;
        this.flag = 0;
    }
    else {
        document.getElementById("b7").value = "0";
        document.getElementById("b7").disabled = true;
        this.flag = 1;
    }
},
 
 myfunc_10() {
    if (this.flag == 1) {
        document.getElementById("b8").value = "X";
        document.getElementById("b8").disabled = true;
        this.flag = 0;
    }
    else {
        document.getElementById("b8").value = "0";
        document.getElementById("b8").disabled = true;
        this.flag = 1;
    }
}
 ,
 myfunc_11() {
    if (this.flag == 1) {
        document.getElementById("b9").value = "X";
        document.getElementById("b9").disabled = true;
        this.flag = 0;
    }
    else {
        document.getElementById("b9").value = "0";
        document.getElementById("b9").disabled = true;
        this.flag = 1;
    }
}
     
                } 
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
input{
    cursor: pointer;
}
h1 {
        color: orangered;
        font-size: 45px;
    }
 
    /* 3*3 Grid */
    #b1, #b2, #b3, #b4, #b5,
    #b6, #b7, #b8, #b9 {
        width: 80px;
        height: 80px;
        margin: auto;
        border: 1px solid gray;
        border-radius: 6px;
        font-size: 60px;
        text-align: center;
    }
 
    /* Reset Button */
    #but { 
    }
 
    /* Player turn space */
    #print {
        font-family: Verdana,
            Geneva, Tahoma, sans-serif;
 
        color: #2b7c58;
        font-size: 20px;
    }
 
    /* Main Container */
    #main {
        text-align: center;
    }
 
    /* Game Instruction Text */
    #ins {
        font-family: Verdana,
            Geneva, Tahoma, sans-serif;
             
        color: #2b7c58;
        font-size: 17px;
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
 cursor: pointer;
}
</style>
