<template>
    <div class="container">
        <div class="box">
            <div id="bgimg"></div>
            <h1>From now on, when you finish answering 2 questions, 
                <br>your favor team must be in place</h1>
            <div class="question">
                <p>Question4：Have you ever been betrayed by someone you believed in？</p>
                <router-link class="yes-button" to="/question5">Yes</router-link>
                <router-link class="no-button" to="/question5" @click.native="increment">No</router-link>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    computed:{
        num(){
            return this.$store.state.count;
        }
    },
    methods:{
    increment(){
    this.$store.state.count++;
    }
},
}

</script>

<style scoped>
.container{
    background-color: rgba(0,0,0,0.6);
    margin: 0;
    padding: 0;
    overflow:hidden;
}

.box{
    position: relative;
}

#bgimg{
    display: flex;
    flex-flow: column;
    justify-content: center;
    align-items: center;
    height: 100vh;
    width: 100%;
    background: url('https://images.unsplash.com/photo-1471295253337-3ceaaedca402?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=800&q=60') top center / cover no-repeat;
    z-index: 1;
    opacity: 0.3;
    position: relative;
}

h1{
    font-weight: bold;
    color:rgb(255, 255, 255);
    width: 100%; 
    height: 1.5em;
    text-align: center;
    position: absolute;
    margin: auto;
    top: 0;
    bottom: 300px;
    z-index: 2;
    animation-name: fadein;
    animation-duration: 2s;
    font-family :Quicksand, sans-serif;/*Google Font*/

}

@keyframes fadein {
from {
    opacity: 0;
    transform: translateY(20px);
}
to {
    opacity: 1;
    transform: translateY(0);
}
}

p{
    font-weight: bold;
    font-size: 20px;
    color:rgb(255, 255, 255);
    width: 100%; 
    height: 1.5em;
    text-align: center;
    position: absolute;
    margin: 0;
    padding: 0;
    top: 50%;
    left: 0%;
    bottom: 0%;
    z-index: 3;
    animation-name: fadein;
    animation-duration: 2s; 
    padding: 0.5em 1em;
    background: -moz-linear-gradient(#5eccc7, #ebf18d);
    background: -webkit-linear-gradient(#ffb03c, #5192e7);
    background: linear-gradient(to right, #0e4af0, #d42020);
    color: #FFF;
}

.yes-button{
position: absolute;
top: 70%;
left: 40%;
-ms-transform: translate(-50%,-50%);
-webkit-transform: translate(-50%,-50%);
transform: translate(-50%,-50%);
/*以下装飾*/
margin:0;/*余計な隙間を除く*/
font-size: 20px;/*文字サイズ*/
border: solid white 2px; /*線で囲う*/
padding: 7px;/*文字と線の間の余白*/
color: white;/*文字色*/
text-decoration: none;/*下線を表示させない*/
z-index: 3;
width: 100px;
text-align: center;
}
.no-button{
position: absolute;
top: 70%;
left: 60%;
-ms-transform: translate(-50%,-50%);
-webkit-transform: translate(-50%,-50%);
transform: translate(-50%,-50%);
/*以下装飾*/
margin:0;/*余計な隙間を除く*/
font-size: 20px;/*文字サイズ*/
border: solid white 2px; /*線で囲う*/
padding: 7px;/*文字と線の間の余白*/
color: white;/*文字色*/
text-decoration: none;/*下線を表示させない*/
z-index: 3;
width: 100px;
text-align: center;
}

a:hover{
    background: rgba(255, 255, 255, 0.3);
}



@media screen and (max-width: 479px) {

h1{
    font-weight: bold;
    color:rgb(255, 255, 255);
    width: 300px; 
    height: 1.5em;
    text-align: center;
    position: absolute;
    margin: auto;
    top: 0;
    bottom: 300px;
    z-index: 2;
    animation-name: fadein;
    animation-duration: 2s;
    font-family :Quicksand, sans-serif;/*Google Font*/
    font-size: 16px;
    left: 10%;
}

p{
font-weight: bold;
font-size: 12px;
color:rgb(255, 255, 255);
width: 100%; 
height: 2.5em;
text-align: center;
position: absolute;
margin: 0;
padding: 0;
top: 50%;
left: 0%;
bottom: 0%;
z-index: 3;
animation-name: fadein;
animation-duration: 2s; 
padding: 0.5em 1em;
background: -moz-linear-gradient(#5eccc7, #ebf18d);
background: -webkit-linear-gradient(#ffb03c, #5192e7);
background: linear-gradient(to right, #20ce4b, #cfd5f3);
color: #FFF;
}

.yes-button{
position: absolute;
top: 70%;
left: 30%;
-ms-transform: translate(-50%,-50%);
-webkit-transform: translate(-50%,-50%);
transform: translate(-50%,-50%);
/*以下装飾*/
margin:0;/*余計な隙間を除く*/
font-size: 12px;/*文字サイズ*/
border: solid white 2px; /*線で囲う*/
padding: 7px;/*文字と線の間の余白*/
color: white;/*文字色*/
text-decoration: none;/*下線を表示させない*/
z-index: 3;
width: 50px;
text-align: center;
}
.no-button{
position: absolute;
top: 70%;
left: 70%;
-ms-transform: translate(-50%,-50%);
-webkit-transform: translate(-50%,-50%);
transform: translate(-50%,-50%);
/*以下装飾*/
margin:0;/*余計な隙間を除く*/
font-size: 12px;/*文字サイズ*/
border: solid white 2px; /*線で囲う*/
padding: 7px;/*文字と線の間の余白*/
color: white;/*文字色*/
text-decoration: none;/*下線を表示させない*/
z-index: 3;
width: 50px;
text-align: center;
}
}

</style>