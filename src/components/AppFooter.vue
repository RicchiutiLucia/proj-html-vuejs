<script>
import AppFooterBottom from './AppFooterBottom.vue';
  export default {
    name: 'AppFooter',
    components:{
        AppFooterBottom
    },
    data(){
      return{
        contact:[
            {
                title: 'COME FINDUS',
                phone: 'Phone: 1.800.555.6789',
                city: 'NewYork. NY 5555',
                email: 'Email: info@your-domain.com',
                street: '12345 North Main Street'
            }

        ],
        
        question:[
           {
            title: 'RECENT POST',
            question_one: 'Train with free weights or your body weight',
            question_two: 'Nutritional advice thath will keep you training'
           }
        ],
        open:[
            {
                
                title: 'OPENING TIMES',
                monday: 'Monday',
                friday: 'Friday',
                saturday: 'Saturday',
                sunday: 'Sunday',
                open: '9:00',
                close1: '19:00',
                close2: '21:00'
            }
        ]

      }
    }
}
</script>

<template>
     <div class="flex container">
    <div class="wrapper-container">
        <div class="wrapper" >
      <div class="wrapper-item" v-for="(contact,index) in contact" :key="index" >
        <h1>{{contact.title}}</h1>
        <p>{{contact.street}}</p>
        <p>{{contact.city}}</p>
        <p>{{contact.phone}}</p>
        <p>{{contact.email}}</p>
      </div> 
    </div>
    <div class="wrapper" v-for="(question,index) in question" :key="index">
      <div class="wrapper-item">
        <h1>{{question.title}}</h1>
        <div class="flex-columns">
          <i class="fas fa-chevron-right"> </i>
          <span class="line-height">{{question.question_one}}</span>
          <hr class="line">
         
        </div>
        <div class="flex-columns">
          <i class="fas fa-chevron-right"> </i>
          <span class="line-height">{{question.question_two}}</span>
          <hr class="line">
          
        </div>
      </div>
    </div>
    <div class="wrapper"  v-for="(open,index) in open" :key="index">
      <div class="wrapper-item">
        <h1>{{open.title}}</h1>
        <div>
          <p>Weekends: {{open.monday}} - {{open.friday}}</p>
          <div class="opening">{{open.open}} - {{open.close1}}</div>
         
        </div>
        <div>
          <p>Weekends: {{open.saturday}} - {{open.sunday}}</p>
          <div class="opening" >{{open.open}} - {{open.close2}}</div>
        </div>
      </div>
    </div>
    <div class="wrapper-image">
      <img  class="image" src="../../gym_ad-compressor.jpg" alt="">
    </div>
  </div>
    </div>

    <AppFooterBottom></AppFooterBottom>
   

</template>

<style lang="scss">
@use '../styles/generals.scss';
@use '../styles/variable.scss';
.container{
    width: 100%;
    background-color: #1f2123;
    .wrapper-container{
        display: flex;
        padding: 20px;
    
    .wrapper-item {
        margin: 50px;
      
        h1 {
          font-size: 13px;
          color: gray;
          margin-bottom: 15px;
        }
        i, span, p {
            color: #999;
            font-size: 11px;
            margin-bottom: 10px;
        }
        i {
            margin-right: 2px;
        }
        .opening{
            font-size: 11px;
            margin-bottom: 10px;
            color:#4a5053;

        }
        .line{
            color: #4a5053;
        }
        .line-height{
            line-height: 20px;
        }
        
        
    }
}

    }
    
   


     

    
</style>

