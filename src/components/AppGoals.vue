<script>
export default{
    name:'AppGoals',
    data(){
        return{

        }
    }
}
</script>
<template>
      <div class="container-goal">
      <div class="container-small-goal">
        <div>
          <h3>Achieve Your Fitness Goals</h3>
          <p>Flexible membership packages to suit all levels of athlete and achive your fitness goals</p>
        </div>
        <div>
        <button>JOIN US</button>
        </div>
      </div>
    </div>

</template>

<style lang="scss">
@import '../styles/generals.scss';
@import '../styles/variable.scss';


.container-goal {
  width: 100%;
  height: 200px;
  background-image: url('../assets/images/home-parallax.jpg');
  background-position: 20% 20%;
    .container-small-goal{
      display: flex;
      justify-content: center;
      align-items: center;
        h3 {
            margin: 80px  0px 0px 0px;
          color: $colorWhite;
        
        }
        p{
            margin-top: 20px;
            color: $colorWhite; 
           
        }
        button {
            margin-top: 80px;
            margin-left: 100px;
            padding-top: 50px;
            border: 1px solid $borderButton; 
            padding: 15px 30px;
            background-color: inherit;
            color: $borderButton;
            cursor: pointer;
        }
        button:hover{
          font-size: 16px;
        }
    }
}

    
</style>