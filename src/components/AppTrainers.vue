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
              <img :src="`../assets/images/trainer-${train.img}.jpg`" alt="">
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
@use '../styles/generals.scss';
@use '../styles/variable.scss';

.container-trainers {
  background-color: #1f2123;
  width: 100%;
    .container-small-trainers {
      width: 60%;
      margin: 0 auto;
      padding: 50px 50px;
        .container-s-trainers-top {
          h2 {
            color: white;
          }
        } 
        .container-s-trainers-bottom {
          display: flex;
          flex-direction: column;
          align-items: center;
            .wrapper-card-trainer {
              display: flex;
                .card-trainer {
                height: 310px;
                margin: 5px 10px 5px 10px;
                  .card-trainer-bottom {
                    padding: 18px 0 18px 18px;
                      .card-trainer-title{
                        width: 175px;
                          h3, h4{
                            color: white;
                            font-size: 13px;
                            line-height: 16px;
                          }
                      }
                      .card-trainer-des {
                        width: 175px;
                          p{
                            padding: 10px 0 10px;
                            color:  #6b6b6b;
                            font-size: 13px;
                            line-height: 16px;
                          } 
                      }
                      .card-trainer-social {
                        width: 175px;
                          i {
                            margin-right: 8px;
                            color: white;
                          }
                      }
                  }
              }
            }
            .btn-trainers{
              padding-top: 50px; 
                button {
                  padding: 10px 10px 10px 10px;
                  background-color: inherit;
                  color:  #6b6b6b;
                }
            } 
        }
    }
}
</style>