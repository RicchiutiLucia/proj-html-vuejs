<script>
export default{
    name:'AppPerformance',
    data(){
        return{
        }
    }
}
</script>

<template>
     <div class="container-performance">
      <div class="container-small-performance">
        <div class="container-small-top flex flex-columns">
          <h2 class="marginB10">HIGH PERFORMANCE FACILITIES</h2>
          <img class="marginB10" src="../assets/images/divider-xx-red.png" alt="">
        </div>
        <div class="wrapper-img-performance">
          <div class="wrapper-card">
            <img src="../assets/images/home-image1.jpg">
            <img src="../assets/images/home-image2.jpg">
            <img src="../assets/images/home-image3.jpg">
            <img src="../assets/images/home-image4.jpg">
            <img src="../assets/images/home-image54.jpg">
            <img src="../assets/images/home-image6.jpg">
          </div>
        </div>
      </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/generals.scss';
@use '../styles/variable.scss';
.container-performance {
width: 100%;
padding: 100px 120px 100px 120px;

background-color: #25292b;
    .container-small-performance{
      width: 100%;
      margin: 0 auto;
      display: flex;
      flex-direction: column;
      justify-content: center;
        .container-small-top {
            h2 {
              color: white;
            }
        }
    }
    .wrapper-img-performance {
      display: flex;
      justify-content: center;
      align-items: center;
      
       .wrapper-card{
         margin: 5px 20px 20px 20px;
         display: flex;
         justify-content: center;
         flex-wrap: wrap;
       }
    img{
        width: 300px;
        margin: 20px;
    }
    }
}
</style>