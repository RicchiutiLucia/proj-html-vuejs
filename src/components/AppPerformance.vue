<script>
export default{
    name:'AppPerformance',
    data(){
        return{
          Performance :
                        [
                            {
                                immagine: 'image1-200x135'
                            },
                            {
                                immagine: 'image2-200x135'
                            },
                            {
                                immagine: 'image3-200x135'
                            },
                            {
                                immagine: 'image4-200x135'
                            },
                            {
                                immagine: 'image54-200x135'
                            },
                            {
                                immagine: 'image6-200x135'
                            }
                        ]
        }
    }
}
</script>

<template>
     <div class="container-performance">
      <div class="container-small-performance">
        <div class="container-small-top flex flex-columns">
          <h2 >HIGH PERFORMANCE FACILITIES</h2>
          <img class="image" src="../assets/images/divider-xx-red.png" alt="">
        </div>
        <div class="wrapper-img-performance">
          <div class="wrapper-card" v-for="(img, index) in Performance" :key="index">
            <img :src="(`./home-${img.immagine}.jpg`)" alt="">
          </div>
        </div>
      </div>
    </div>
</template>

<style lang="scss" scoped>
@import '../styles/generals.scss';
@import '../styles/variable.scss';

.container-performance {
width: 100%;
padding: 100px 120px 100px 120px;

background-color: $backgroundGrayLight;
    .container-small-performance{
      width: 100%;
      margin: 0 auto;
      display: flex;
      flex-direction: column;
      justify-content: center;
        .container-small-top {
            h2 {
              color: $colorWhite;
              padding: 30px;
            }
            .image{
              margin-bottom: 20px;
            }
        }
    }
    .wrapper-img-performance {
      display: flex;
      justify-content: center;
      align-items: center;
      flex-wrap: wrap;
      
       .wrapper-card{
         margin: 5px 20px 20px 20px;
         display: flex;
         justify-content: center;
         flex-wrap: wrap;
       }
        img{
            width: 250px;
            margin: 20px;
        }
        img:hover{
          box-shadow:  10px  10px 5px rgb(88, 101, 108),
                      -10px -10px 5px rgb(88, 101, 108),
                       10px -10px 5px rgb(88, 101, 108),
                      -10px  10px 5px rgb(88, 101, 108);
        }
    }
}
</style>