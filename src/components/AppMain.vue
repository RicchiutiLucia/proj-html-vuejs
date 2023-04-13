<template>

  <AppCLass></AppCLass>
  <AppForm></AppForm>
  <AppActivity></AppActivity>
  <AppResultWorld></AppResultWorld>
  <AppPerformance></AppPerformance>
  <AppCitazione></AppCitazione>
  <AppTrainers></AppTrainers>
  <AppNews></AppNews>
  <AppGoals></AppGoals>
   
      
</template>
    
<script>
import AppForm from './AppForm.vue';
import AppCLass from './AppClass.vue';
import AppActivity from './AppActivity.vue';
import AppResultWorld from './AppResultWorld.vue';
import AppPerformance from './AppPerformance.vue';
import AppCitazione from './AppCitazione.vue';
import AppTrainers from './AppTrainers.vue';
import AppNews from './AppNews.vue';
import AppGoals from './AppGoals.vue';

  export default {
    name: 'AppMain',
    data(){
      return{
      }
    },
    components:{
      AppForm,
      AppCLass,
      AppActivity,
      AppResultWorld,
      AppPerformance,
      AppCitazione,
      AppTrainers,
      AppNews,
      AppGoals
    }
}
</script>
    
<style lang="scss">
@use '../styles/generals.scss';
@use '../styles/variable.scss';

    
</style>