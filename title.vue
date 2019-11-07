<template>
    <div>
        <div class="container">
       
            <div class="row">
                <div class="col-xs-12 col-sm-6">
                <div class="txtBlock"><p class="txtPosition">This is a page for <br> potato voting</p>
                </div>
                </div>
                <div class="col-xs-12 col-sm-6">
                <div class="imgBlock"><p class="txtPositionimg">made by with love <br> by [name]</p></div>
                </div>
            </div>


            <div class="bottmBlock">
            <div class="row">
                
            <div class="col-sm-3"></div>

            <div class="col-sm-6">
            <div class="row likeBlock">
                <div class="col-xs-12 col-sm-6">
            <img class="mashed" src="../assets/mashedPotato.jpg" alt="mashedPotato">
                </div>
                
                 <div class="col-sm-6 likeBlockTxt">
                     
            <button @click="likes += 1" class="likebtn">LIKE</button> <span class="txtstyl">Likes: {{ likes }}</span>
                 </div>
            </div>
           

              <div class="row dislikeBlock">
                 <div class="col-sm-6">
            <img class="mashed" src="../assets/bakedPotato.jpeg" alt="bakedPotato">
                </div>
                <div class="col-sm-6 dislikeBlockTxt">
            <button @click="dislikes += 1" class="dislikebtn">DISLIKE</button> <span class="txtstyl">Dislikes: {{ dislikes }}</span>
                </div>
              </div>
            
     
          <div class="row">
             <div class="col-sm-3"></div>
            <div class="col-sm-6 resetSpace">  
            <button @click="resetAll" class="rstbtn">RESET</button> 
            
            <span class="txtstyl">Total Clicks: {{ likes + dislikes }}</span>
            </div>
          <div class="col-sm-3"></div>

            </div>

            </div>

            <div class="col-sm-3"></div>
            </div>
           </div>
      
            
            
        </div>
    </div>
</template>

<script>
export default {
    data () {
        return {
            likes: 0,
            dislikes: 0
        }
    },

    methods: {
        resetAll() {
            this.likes = 0
            this.dislikes = 0
        }
    }
}
</script>

<style>
*{
    padding:0px;
    margin:0px;
}



.txtBlock{
    background:#4792b2;
   
    height:500px;
    text-align: center;
    color: black;
    font-size: 30px;
    text-decoration: underline;
    position: relative;
  
}
.txtPosition{
    position: relative;
    top: 38%;
    /* left: 50%; */
    color: black;
    font-size: 30px;
    text-decoration: underline;
    text-align: center;
}
.txtPositionimg{
        position: relative;
    top: 38%;
    /* left: 30%; */
    color: black;
    font-size: 30px;
    font-style: italic;
    text-align: center;
    
}

.txtstyl{
    color:yellow;
}
.imgBlock{
    background-image: url('../assets/thumbs.png' );
  
    height:500px;
    position: relative;
     text-align: center;
   
}

.likebtn{
    background: greenyellow;
    width:80px;
    border-radius: 7px;
}
.likebtn:hover{
    background: green;
    color:white;
}

.dislikebtn{
     background: tomato;
    width:80px;
    border-radius: 7px;
}
.dislikebtn:hover{
    background: red;
    color:white;
}
.rstbtn{
     background: lightyellow;
    width:80px;
    border-radius: 7px;
}
.rstbtn:hover{
    background: yellow;
    color:black;
}
.bottmBlock{
    background: black;
    padding:25px;
}

.mashed{
    width:190px;
    height:130px;
    margin-left: 48px;;
    
}

.txtstyl{
    color:white;
    margin-left: 20px;
}
.rst{
    margin-left: 95px;
}
.variant :active{
    background: lightslategray;
}
.liked{
    margin-bottom:15px;
}
.likebtnsco{
    padding-top:4px;
}

.likeBlock{
    margin-bottom: 20px;
}
.dislikeBlock{
    margin-bottom: 20px; 
}
.likeBlockTxt{
    padding-top: 45px;
    padding-left: 70px !important;
}
.dislikeBlockTxt{
     padding-top: 45px;
    
    padding-left: 70px !important;
}
.resetSpace{
    margin-left: 60px;
}
</style>


