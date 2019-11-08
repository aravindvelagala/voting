<template>
  <div class="mainstream">
      
    <b-container class="bv-example-row">
      <b-row>
        <b-col sm="6" class="head">
          <h3>This is a page for potato voting</h3>
        </b-col>
        <b-col sm="6" class="likes"></b-col>
      </b-row>
    </b-container>
    <b-container  class="mas" >
        <b-row>
        <b-col sm="6" offset="3">
        <b-nav >
    <b-nav-item><img src="https://raw.githubusercontent.com/cognitedata/fe-interview-challenge-vue/master/resources/mashedPotato.jpg" width="150" height="90"></b-nav-item>
    <div class="red">
    <b-nav-item> <b-button @click="likes+=1" variant="success">Like</b-button></b-nav-item>
    >
    <b-nav-item><span style="color:white">Likes:{{likes}}</span></b-nav-item>
    
    </div>

    </b-nav>
        </b-col>
    </b-row>

    <b-row>
        <b-col sm="6" offset="3" >
    <b-nav >
    <b-nav-item><img src=https://raw.githubusercontent.com/cognitedata/fe-interview-challenge-vue/master/resources/bakedPotato.jpeg width="150" height="90"></b-nav-item>
    <div class="green">
    <b-nav-item> <b-button @click="dislikes+=1" variant="danger">Dislike</b-button></b-nav-item>
   
    <b-nav-item><span style="color:white">dislikes:{{dislikes}}</span></b-nav-item>
    
    </div>

    </b-nav>
      </b-col>
    </b-row>

    <b-row>
        <b-col sm="6" offset="4">
    <b-nav>
    <b-nav-item><b-button @click="resetbtn" variant="warning">Reset</b-button></b-nav-item>
    <b-nav-item><span style="color:white">Total Clicks:{{likes+dislikes}}</span></b-nav-item>
    </b-nav>
        </b-col>
    </b-row>
</b-container>
    
    
  </div>
  
</template>
<script>
export default {
    data() {
        return {
           likes: 0,
      dislikes: 0
       }
    },
    methods: {
        resetbtn(){
           (this.likes=0),(this.dislikes=0);
        }

    }
};
</script>
<style scoped>
.head {
  height: 40vh;
  background-color: darkslateblue;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}
.likes {
  background-image: url('https://raw.githubusercontent.com/cognitedata/fe-interview-challenge-vue/master/resources/thumbs.png');
  width:100px;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  height: 40vh; 
}
.mas {
    background-color: black;
    padding: 100px;
    }
 .red {
    margin-top: 30px;
    display: flex;
 }   
 .green {
   margin-top: 30px;
   display: flex;
 }
 /* .likes {
   margin-top: 20px;
 }

 .dislikes {
   margin-top: 20px;
 } */



</style>