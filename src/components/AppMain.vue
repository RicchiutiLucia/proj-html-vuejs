<template>

  <AppCLass></AppCLass>
  <AppForm></AppForm>
   
      
</template>
    
<script>
import AppForm from './AppForm.vue';
import AppCLass from './AppClass.vue';

  export default {
    name: 'AppMain',
    data(){
      return{
      }
    },
    components:{
      AppForm,
      AppCLass
    }
}
</script>
    
<style lang="scss">
@import '../styles/generals.scss';
@import '../styles/variable.scss';

    
</style>