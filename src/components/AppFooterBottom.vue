<template>
    <div class="container-bottom">
      <div class="left height110 flex"  v-for="(proprerty,index) in proprerty" :key="index">
        <div class="flex-center-items" >
          <i class="far fa-copyright marginR5"></i>
          <p>{{proprerty.copyright}}</p>
        </div>
        <p>{{proprerty.theme}}</p>
        <p>{{proprerty.right}}</p>
        <p>{{proprerty.createWith}}</p>
      </div>
      <div class="right">
        <ul class="flex height110 ">
          <li v-for="(element,index) in social" :key="index">
            <a>
             <i :class="`fab ${element.icon}`"></i>
            </a>
          </li>
        </ul>
      </div>
    </div>
  </template>
  
  <script>

  export default {
    name: 'FooterBottom',
    data() {
      return {
        proprerty:[
            {
                copyright: 'Copyright 2012-2020',
                theme: 'Avada theme by Theme Fusion' ,
                right: 'All Rights reserved',
                createWith: 'Powered by Wordpress'
            }
        ],
        social:[
            {
                prefix: 'fab',
                icon: 'fa-facebook-square'
            },
            {
                prefix: 'fab',
                icon: 'fa-twitter-square'
            },
            {
                prefix: 'fab',
                icon: 'fa-instagram-square'
            }
        ],
      }
    }
  }
  </script>
  

<style lang="scss" scoped >
@import '../styles/generals.scss';
@import '../styles/variable.scss';
.container-bottom{
    background-color: $colorLightBlack;
    display: flex;
    justify-content: space-around;
    padding: 30px;
    .left {
        margin-left: 30px;
      i {
        color: $colorGrey;
        font-size: 10px;
      }
      i:hover{
        color: $colorOrange;
      }
      p {
        color: $colorGrey;
        font-size: 10px;
          &::after {
            content: ' |';
            margin: 10px;
        }
      }
      p:hover{
        color: $colorOrange;
      }
      
      
 }
  .right{
      li {
        list-style-type: none;
          i {
            margin-right: 10px;
            font-size: 25px;
            color: $colorOrange;
          }
          i:hover{
            font-size: 30px;
          }
      }
  }

}
  
</style>