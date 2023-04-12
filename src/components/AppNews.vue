<script>
export default{
    data(){
        return{
            news :
                    [
                        {
                            img: 'blog1-200x104.jpg',
                            title: 'Train with free weights or your body weight?',
                            description: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Saepe, consequatur, architecto aliquid itaque'
                        },
                        
                        {
                            img: 'blog6-200x200.jpg',
                            title: 'Nutritional advice that will keep your training',
                            description: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Saepe, consequatur, architecto aliquid itaque'
                        },
                        {
                            img: 'trainer4-200x148.jpg',
                            title: 'Top 5 mistakes every gym member makes',
                            description: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Saepe, consequatur, architecto aliquid itaque'
                        },
                        {
                            img: 'trainer3-200x148.jpg',
                            title: 'Simple principles for you next workout',
                            description: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Saepe, consequatur, architecto aliquid itaque'
                        },
                        {
                            img: 'blog4-200x144.jpg',
                            title: "To be number one, train like you're number two",
                            description: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Saepe, consequatur, architecto aliquid itaque'
                        },
                        {
                            img: 'trainer1-200x148.jpg',
                            title: 'The myths of shedding body fat explored',
                            description: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Saepe, consequatur, architecto aliquid itaque'
                        }
                    ]

        }
    }
}
</script>
<template>
      <div class="container-news">
      <div class="container-small-news">
        <div class="container-s-news-top">
          <h2 class="marginB10">PERFORMANCE NEWS</h2>
          <img class="marginB10" src="../assets/images/divider-xx-red.png" alt="">
        </div>
        <div class="container-s-news-bottom">
          <div class="wrapper-card-news">
            <div class="card-news" v-for="(element,index) in news" :key="index">
              <div class="cont-s-n-bot-top">
                <img :src="`./${element.img}`" alt="">
              </div>
              <div class="cont-s-n-bot-bot">
                <h3>{{element.title}}</h3>
                <p>{{element.description}}</p>
              </div>
              
            </div>
          </div>
        </div>
        <button>READ ALL ARTICLES</button>
      </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/generals.scss';
@use '../styles/variable.scss';

.container-news {
  background-color: #252a2d;
  width: 100%;
  padding: 50px 50px;
    .container-small-news{
      width: 60%;
      margin: 0 auto;
      .container-s-news-top {
        width: 100%;
        display: flex;
        flex-direction: column;
        align-items: center;
        h2{
            color: white;
        }
      }
      .container-s-news-bottom {
          .wrapper-card-news {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
              .card-news {
                background-color: #1f2123;
                margin: 10px 10px 10px 10px;
                width: 250px;
                height: 100%;
                img{
                    width: 100%;
                }
                  .cont-s-n-bot-bot {
                    padding: 15px 15px 15px 15px;
                    h3{
                        color: white;
                    }
                    p{
                        color:grey;
                        font-size: 13px;
                        padding-top: 10px;
                    }
                  }
              }
          }
      }
    }
    button {
        padding-top: 50px;
        text-align: center;
        border: 1px solid gray; 
        padding: 10px 30px;
        background-color: inherit;
        color: gray;
        cursor: pointer;
      
    }
}


    
</style>
