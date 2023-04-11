<template>
     <div class="container height400">
      <div class="container-small height100">
        <!-- Inserendo contenuto posso eliminare le altezze fisse e rendere il tutto dinamico -->
        <div class="flex height350"> <!-- Utilizzando flex con un div mancante, avrei perso elasticità-->
          <div class="height200  marginR10">
            <img class="width400" src="../assets/images/home_img-compressor.jpg" alt="">
          </div>
          <div class="height200 width300 marginL50">
            <h3 class="marginB10 font-s18 colorWhite">Sign Up For A Free Training Sessione!</h3>
            <form class="d-flex flex-columns">
              <label for="name">Name <abbr title="campo obbligatorio">*</abbr></label>
              <input type="text" name="name" placeholder="">
              <label for="e-mail">E-mail</label>
              <input type="text" email="e-mail" placeholder="">
              <input type="submit" value="START NOW !" class="btn">
            </form>
          </div>
        </div>
      </div>
    </div>

    
</template>
  
<script>
export default {
  name: 'AppForm',
  data(){
    return{
    }
  }
}
</script>
  
<style lang="scss" scoped>
@import '../styles/generals.scss';
@import '../styles/variable.scss';
.container{
    background-color: #1f2323;
}
h3{
    color: $colorWhite;
    padding-bottom: 20px;
}
input {
    width: 100%;
    padding: 12px 20px;
    margin: 8px 0;
    display: inline-block;
    border: 1px solid #ccc;
    border-radius: 2px;
    box-sizing: border-box;
    background-color: $colorDarkGrey;
    
}
.btn{
    background-color: #ee6059;
    color: $colorWhite;
}
label{
    color: lightgray;
    font-size: 14px;
    margin: 5px 0px;
}


  
</style>