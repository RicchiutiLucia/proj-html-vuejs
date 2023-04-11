<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';

export default {
  name: 'App',
  components: {
    AppHeader,
    AppMain
  }
}


</script>

<template>
    <body>
        <div class="background container height728">
            <AppHeader/>
        <div class="container-small heightBanner flex-center">
            <div class="container-Title">
                <h1 class="title">NO PAIN NO GAIN</h1>
                <p>Motivation is what gets you started. Habit is what keeps you going </p>
                <button>JOIN US TODAY</button>
            </div>
        </div>
        </div>

        <AppMain></AppMain>

        
    </body>
    
  
</template>

<style lang="scss">
@import './styles/generals.scss';
@import './styles/_variable.scss';
.background {
  background-image: url('assets/images/home-banner.jpg');
  background-size: cover;
}
.container {
  width: 100%;
}
.title {
  font-size: $fontSize65;
  color: $colorWhite;
  font-weight: bold;
}
.container-Title {
  margin-top: 75px;
  color: $colorWhite;
  text-align: center;
    p {
      font-size: 16px;
      color: lightgray;
      padding: 15px 15px
    }
    button {
      border: 1px solid gray; 
      padding: 10px 30px;
      background-color: inherit;
      color: gray;
      cursor: pointer;
    }
}

</style>
