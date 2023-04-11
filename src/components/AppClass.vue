<script>

  export default {
    name: 'AppCLass',
    data(){
      return{
      }
    },
    
}
</script>
<template>
    <div class="container height300 bg">
    <div class="container-small height100 flex">
      <div class="container-Title">
        <h2>WORLD CLASS Fitness</h2>
        <a href="#"><img src="../assets/images/divider-xx-red.png"></a>
        <p>At Avada Gym, everything we do from top to bottom is of the highest quality to ensure we're equipped
        to help you reach your goals of a healthy and fit lifestyle.</p>
      </div>
    </div>
  </div>
</template>
<style lang="scss" scoped>
@import '../styles/generals.scss';
@import '../styles/variable.scss';

.container-Title {
  width: 860px;
  margin-top: 75px;
  color: $colorWhite;
  text-align: center;
    h2{
        font-weight: bold;
    }
    a img{
        margin-top: 30px;
    }
    p {
      font-size: 16px;
      color: lightgray;
      margin-top: 10px;
      padding: 15px 15px;
      line-height: 40px;
    }
  
}
.bg{
    background-color: $colorDarkGrey;
}
 
    
</style>
  