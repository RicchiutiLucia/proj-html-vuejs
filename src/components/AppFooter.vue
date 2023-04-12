<script>
import FooterTop from './FooterTop.vue';

export default{
    data(){
        return{
            contacts:[
                            {
                                title: 'COME FINDUS',
                                phone: 'Phone: 1.800.555.6789',
                                city: 'NewYork. NY 5555',
                                email: 'info@your-domain.com',
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
    },
    components:{
        FooterTop,
       
    }
}
</script>

<template>
     <div class="container">
      <div class="container-small wrapper">
        <FooterTop 
        />
      </div>
    </div>  
    <div class="container height110">
      <div class="container-small height100">
        
      </div>
    </div>
 

</template>

<style lang="scss">
@use '../styles/generals.scss';
@use '../styles/variable.scss';
.container{
    background-color: #25292b;
}
</style>