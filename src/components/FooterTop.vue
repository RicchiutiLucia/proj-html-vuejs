<script>
export default{
    data(){
        return{
            
        }
    },
    props:{
        contacts: Array,
        question:Array,
        open:Array
    }
}
</script>

<template>
     <div class="flex-center-items flex">
    <div class="wrapper">
      <div class="wrapper-item" v-for="(contact, index) in contacts" :key="index">
        <h1>{{contact.title}}</h1>
        <p>{{contact.street}}</p>
        <p>{{contact.city}}</p>
        <p>{{contact.phone}}</p>
        <p>{{contact.email}}</p>
      </div> 
    </div>
    <div class="wrapper">
      <div class="wrapper-item"  v-for="(question, index) in question" :key="index">
        <h1>{{question.title}}</h1>
        <div class="flex-center-items">
          <i class="fas fa-chevron-right"></i>
          <p>{{question.question_one}}</p>
        </div>
        <div class="flex-center-items">
          <i class="fas fa-chevron-right"></i>
          <p>{{question.question_two}}</p>
        </div>
      </div>
    </div>
    <div class="wrapper">
      <div class="wrapper-item"  v-for="(open, index) in open" :key="index">
        <h1>{{open.title}}</h1>
        <div>
          <p>Weekends {{open.monday}} - {{open.friday}}</p>
          <p>{{open.open}} - {{open.close1}}</p>
        </div>
        <div>
          <p>Weekends {{open.saturday}} - {{open.sunday}}</p>
          <p>{{open.open}} - {{open.close2}}</p>
        </div>
      </div>
    </div>
    <div class="wrapper">
      <img src="../assets/images/gym_ad-compressor.jpg" alt="">
    </div>
  </div>

</template>

<style lang="scss">
@use '../styles/generals.scss';
@use '../styles/variable.scss';

.wrapper {
  width: calc(100% / 4);
  height: 100%;
    .wrapper-item {
      width: 80%;
        h1 {
          font-size: 16px;
          color: gray;
          margin-bottom: 15px;
        }
        i, p {
            color: #6b6b6b;
        }
        i {
            font-size: 13px;
            margin-right: 3px;
        }
    }
}
     

</style>