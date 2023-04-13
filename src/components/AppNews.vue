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
          <h2>PERFORMANCE NEWS</h2>
          <img src="../assets/images/divider-xx-red.png" alt="">
        </div>
        <div class="container-s-news-bottom">
          <div class="wrapper-card-news">
            <div class="card-news" v-for="(element,index) in news" :key="index">
              <div class="cont-s-n-bot-top">
                <img class="image" :src="`./${element.img}`" alt="">
              </div>
              <div class="cont-s-n-bot-bot">
                <h3>{{element.title}}</h3>
                <p>{{element.description}}</p>
              </div>
              
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="btn">
        <button>READ ALL ARTICLES</button>
    </div>
</template>

<style lang="scss" scoped>
@import '../styles/generals.scss';
@import '../styles/variable.scss';


.container-news {
  background-color: $backgroundShark;
  width: 100%;
  padding: 50px 50px;
    .container-small-news{
      width: 60%;
      margin: 0 auto;
      .container-s-news-top {
        margin-top: 20px;
        width: 100%;
        display: flex;
        flex-direction: column;
        align-items: center;
        h2{
            color: $colorWhite;
            margin-bottom: 20px;
        }
        img{
          margin-bottom: 30px;
        }
        
      }
      .container-s-news-bottom {
          .wrapper-card-news {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
              .card-news {
                background-color: $backgroundDarkGray;
                margin: 10px 10px 10px 10px;
                width: 250px;
                height: 100%;
                img{
                    width: 100%;
                    
                }
                
                .cont-s-n-bot-top img:hover{
                  opacity: 0.3;
                }
                  .cont-s-n-bot-bot {
                    padding: 15px 15px 15px 15px;
                    h3{
                        color: $colorWhite;
                    }
                    p{
                        color:$colorParagrafo;
                        font-size: 13px;
                        padding-top: 10px;
                    }
                  }
              }
          }
      }
    }
    
}
.btn{
  background-color: #252a2d;
  text-align: center;
  button {
  padding-top: 50px;
  border: 1px solid gray; 
  padding: 10px 30px;
  background-color: inherit;
  color: gray;
  cursor: pointer;
  margin-bottom: 100px;
      
  }
  button:hover{
    font-size: 16px;
  }
}
.d-block{
  display: block;
}
.d-none{
  display: none;
}



    
</style>
