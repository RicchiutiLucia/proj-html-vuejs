<script>
export default{
    name: 'AppResultWorld',
    data(){
        return{
            testimonial:[
                            {
                                img: 'review_1-compressor.jpg',
                                descrition: 'lorem ipsus',
                                name: 'Tara Smith'
                            },
                            {
                                img: 'review_3-compressor-2.jpg',
                                descrition: 'lorem ipsus',
                                name: 'Simon Chel'
                            },
                            {
                                img: 'review_2-compressor.jpg',
                                descrition: 'lorem ipsus',
                                name: 'Jen Wirth'
                            },
                            {
                                img: 'review_4-compressor-2.jpg',
                                descrition: 'lorem ipsus',
                                name: 'Jeff Glum'
                            },
                        ]
        }
    }
}
</script>

<template>
    <div class="container-real-world">
      <div class="container-small-real-world">
        <div class="container-small-top flex flex-columns">
          <h2 class="marginB10">REAL WORLD RESULTS</h2>
          <img class="image" src="../assets/images/divider-xx-red.png" alt="">
        </div>
        <div class="wrapper-testimonials">
          <div class="wrapper-card-testimonial" v-for="(testim, index) in testimonial" :key="index">
            <div class="wrapper-img">
              <img class="height110" :src="`../assets/images/${testim.img}`" alt="">
            </div>
            <div class="wrapper-name paddingBottom20 paddingTop20">
              <p>{{testim.descrition}}</p>
              <h4>{{testim.name}}</h4>
            </div>
          </div>
        </div>
      </div>
    </div>

</template>

<style lang="scss" scoped>
@use '../styles/generals.scss';
@use '../styles/variable.scss';

.container-real-world {
width: 100%;
height: 550px;
background-color: #25292b;
    .container-small-real-world {
      height: 100%;
      width: 80%;
      margin: 0 auto;
      display: flex;
      flex-direction: column;
      justify-content: center;
        .container-small-top {
          h2 {
            color: white;
            
          }
        }
        .wrapper-testimonials{
          display: flex;
          justify-content: center;
          flex-wrap: wrap;
            .wrapper-card-tesimonial {
              display: flex;
              background-color: #1f2123;
              width: 480px;
              margin: 10px;
          }
        }
        
    }
}

</style>