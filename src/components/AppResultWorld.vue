<script>
export default{
    name: 'AppResultWorld',
    data(){
        return{
            testimonial:[
                            {
                                img: 'review_1-compressor.jpg',
                                descrition: '"The trainers at Avada Gym have helped mereach my fitness goals beyond anything I could of hoped for.I love it!"',
                                name: '- Tara Smith'
                            },
                            {
                                img: 'review_3-compressor-2.jpg',
                                descrition: '"The atmosphere at Avada Gym is amazing, thepeople are even better. All in all, it is a great place to work out"',
                                name: '- Simon Chel'
                            },
                            {
                                img: 'review_2-compressor.jpg',
                                descrition: 'The facilities at Avada Gym stood out to me the ost They are well maintained and have high quality equipment "',
                                name: '- Jen Wirth'
                            },
                            {
                                img: 'review_4-compressor-2.jpg',
                                descrition: '"No bad things to say about Avada Gym, they are top notch at every corner and truly take care Of their customers. "',
                                name: '- Jeff Glum'
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
            <div class="wrapper-img ">
              <img  :src="`./${testim.img}`" alt="">
            </div>
            <div class="wrapper-name">
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
height: 700px;
background-color: #25292b;
padding: 100px 120px 100px 120px;
    .container-small-real-world {
      height: 100%;
      width: 100%;
      margin: 0 auto;
      display: flex;
      flex-direction: column;
      justify-content: center;
        .container-small-top {
          h2 {
            color: white;
            margin-top: 50px;
            
          }
        }
        .wrapper-testimonials{
          padding: 50px;
          display: flex;
          flex-wrap: wrap;
          justify-content: center;
          align-items: center;
            .wrapper-card-testimonial{
              background-color: #1f2123;
              margin: 5px 20px 20px 20px;
              padding: 20px;
              width: 450px;
              display: flex;
                img {
                  width: 150px;
                  justify-content: flex-start;
                }
                h4{
                  color: white;
                  font-size: 12px;
                  padding: 15px;
                  color:#aaa9a9;
                }
                p{
                  color: white;
                  font-size: 12px;
                  padding: 15px;
                  line-height: 20px;
                  color:#aaa9a9;
                  font-style: italic;
                  
                }
            }
        }
        
        
    }
}

</style>