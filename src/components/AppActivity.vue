<script>


  export default {
    name: 'AppActivity',
    data(){
      return{
        activity:[
                    {
                        icon: 'fa-link-slash',
                        title: 'Strength & Conditioning',
                        text: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit.'
                    },
                    {
                        icon: 'fa-bicycle',
                        title: 'Fitness & Cardio',
                        text: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit.'
                    },
                    {
                        icon: 'fa-cloud',
                        title: 'Flexibility & Rest',
                        text: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit.'
                    },
                    {
                        icon: 'fa-heart-pulse',
                        title: 'Health & Diet',
                        text: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit.'
                    },
                ]
                    }
                    }
}
</script>


<template>
     <div class="backActivities height350">
      <div class="container-small height100">
        <div class="wrapper-Activities" v-for="(activity,index) in activity" :key="index"> 
          <div class="cycleIcon flex marginB10">
            <i class="largeIcon" :class="`fas ${activity.icon}`"></i>
          </div>
          <h3 class="marginB10 text-white">{{activity.title}}</h3>
          <img class="marginB10" src="../assets/images/divider-x-red.png" alt="">
          <p class="marginB10 text-grey">{{activity.text}}</p>
        </div>
      </div>
    </div>

</template>

<style lang="scss" scoped>
@use '../styles/generals.scss';
@use '../styles/variable.scss';

.backActivities {
  background-image: url('../assets/images/gym_bkgd_bw-compressor.jpg');
  background-position: center;
  .container-small {
    display: flex;
    .wrapper-Activities {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
        .cycleIcon {
          width: 60px;
          height: 60px;
          border: 1px solid #d5625f;
          border-radius: 50%;
            .largeIcon{
              font-size: 30px;
              color: #ee6059;
            }
        }
        p {
          text-align: center;
        }
    }
  }
}

</style>