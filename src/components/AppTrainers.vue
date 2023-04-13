<script>
  export default {
    name: 'AppTrainers',
    data(){
      return{
        dataTrainers :
                    [
                        {   
                            img: '1',
                            title: 'Ann Baker',
                            subTitle: 'Personal Trainer',
                            description: 'lorem ipsum sit amet, consectetur adipiscing elit. In ague nisl, onare volutpat',
                            facebook: 'fa-facebook-square',
                            twitter: 'fa-twitter-square',
                            instagram: 'fa-instagram-square'
                        },
                        {   
                            img: '3',
                            title: 'Anne Warren',
                            subTitle: 'Personal Trainer',
                            description: 'lorem ipsum sit amet, consectetur adipiscing elit. In ague nisl, onare volutpat',
                            facebook: 'fa-facebook-square',
                            twitter: 'fa-twitter-square',
                            instagram: 'fa-instagram-square'
                        },
                        {   
                            img: '4',
                            title: 'Peter Rice',
                            subTitle: 'Personal Trainer',
                            description: 'lorem ipsum sit amet, consectetur adipiscing elit. In ague nisl, onare volutpat',
                            facebook: 'fa-facebook-square',
                            twitter: 'fa-twitter-square',
                            instagram: 'fa-instagram-square'
                        }
                    ]
      }
    }
}
</script>

<template>
     <div class="container-trainers">
      <div class="container-small-trainers">
        <div class="container-s-trainers-top flex flex-columns">
          <h2 class="marginB10">MEET OUR TRAINERS</h2>
          <img class="marginB10" src="../assets/images/divider-xx-red.png" alt="">
        </div>
        <div class="container-s-trainers-bottom">
          <div class="wrapper-card-trainer">
            <div class="card-trainer" v-for="(train, index) in dataTrainers" :key="index">
              <img :src="`./trainer${train.img}.jpg`" alt="">
              <div class="card-trainer-bottom">
                <div class="card-trainer-title">
                  <h3>{{train.title}}</h3>
                  <h4>{{train.subTitle}}</h4>
                </div>
                <div class="card-trainer-des">
                  <p>{{train.description}}</p>
                </div>
                <div class="card-trainer-social">
                  <i :class="`fab ${train.facebook}`"></i>
                  <i :class="`fab ${train.twitter}`"></i>
                  <i :class="`fab ${train.instagram}`"></i>
                </div>
              </div>
            </div>
          </div>
          <div class="btn-trainers">
            <button>VIEW ALL TRAINERS</button>
          </div>
        </div>
      </div>
    </div>

</template>

<style lang="scss" scoped>
@import '../styles/generals.scss';
@import '../styles/variable.scss';


.container-trainers {
  background-color: $backgroundDarkGray;
  width: 100%;
    .container-small-trainers {
      width: 65%;
      margin: 0 auto;
      padding: 50px 50px;
        .container-s-trainers-top {
          h2 {
            color: $colorWhite;
            padding-bottom: 10px;
          }
        } 
        .container-s-trainers-bottom {
          display: flex;
          flex-direction: column;
          align-items: center;
            .wrapper-card-trainer {
              display: flex;
              padding: 30px;
                .card-trainer {
                 
                height: 310px;
                margin: 5px 10px 5px 10px;
                img{
                  width: 100%;
                }
                img:hover{
                  box-shadow: 0px 10px 5px rgb(88, 101, 108);
                  }
                  .card-trainer-bottom {
                    background-color: $backgroundGrayLight;
                    padding: 18px 0 18px 18px;
                      .card-trainer-title{
                       padding: 10px 0px;
                          h3, h4{
                            color: $colorWhite;
                            font-size: 13px;
                            line-height: 16px;
                          }
                      }
                      .card-trainer-des {
                        padding: 10px 0px;
                          p{
                            padding: 10px 0 10px;
                            color:  $colorDoveGray;
                            font-size: 13px;
                            line-height: 16px;
                          } 
                      }
                      .card-trainer-social {
                          i {
                            margin-right: 8px;
                            color: $colorWhite;
                            background-color: $backgroundDarkGray;
                          }
                      }
                  }
              }
            }
            .btn-trainers{
              padding-top: 100px; 
                button {
                  padding-top: 50px;
                  border: 1px solid gray; 
                  padding: 10px 30px;
                  background-color: inherit;
                  color: gray;
                  cursor: pointer;
                }
                button:hover{
                  font-size: 16px;
                }
            } 
        }
    }
}
</style>