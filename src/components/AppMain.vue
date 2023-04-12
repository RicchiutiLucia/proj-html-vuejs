<template>

  <AppCLass></AppCLass>
  <AppForm></AppForm>
  <AppActivity></AppActivity>
  <AppPerformance></AppPerformance>
   
      
</template>
    
<script>
import AppForm from './AppForm.vue';
import AppCLass from './AppClass.vue';
import AppActivity from './AppActivity.vue';
import AppResultWorld from './AppResultWorld.vue';
import  AppPerformance from './AppPerformance.vue';

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
      AppPerformance
    }
}
</script>
    
<style lang="scss">
@use '../styles/generals.scss';
@use '../styles/variable.scss';

    
</style>