<script>
</script>

<template>
     <div class="container-citation">
      <div class="container-small-citation">
        <div>
         <p>"I fear not the man who was has practiced 10,000 <br>
            kicks once, but I fear the man who <br>
             has practiced one kick 10,000 times"</p>
        </div>
        <div class="image">
            <img  src="../assets/images/divider-white-xx.png" alt="">
        </div>
        <div>
          <h3>BRUCE LEE - QUOTE OF THE DAY</h3>
        </div>
      </div>
    </div>
</template>
<style lang="scss" scoped>
@import '../styles/generals.scss';
@import '../styles/variable.scss';

.container-citation {
  background-image: url('../assets/images/home-testimonial-bg.jpg');
  background-position: center;
  background-size: cover;
  height: 500px;
  width: 100%;
    .container-small-citation {
      width: 100%;
      height: 100%;
      margin: 0 auto;
      display: flex;
      flex-direction: column;
      justify-content: center;
        .image{
            text-align: center;
            padding-bottom: 40px;
        }
        p {
          font-size: 20px;
          color: $colorWhite;
          text-align: center;
          padding-bottom: 40px;
          line-height: 40px;
        }
        h3 {
          font-size: 14px;
          color: $colorWhite;
          text-align: center;
        }
    }
}
</style>