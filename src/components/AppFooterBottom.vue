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
  

  <style scoped lang="scss">
@use '../styles/generals.scss';
@use '../styles/variable.scss';
.container-bottom{
    background-color: #1a1c1e;
    display: flex;
    justify-content: space-around;
    padding: 30px;
    .left {
        margin-left: 50px;
      i {
        color: #999999;
        font-size: 10px;
      }
      p {
        color: #999999;
        font-size: 10px;
          &::after {
            content: ' |';
            margin: 10px;
        }
      }
      
      
 }
  .right{
      li {
        list-style-type: none;
          i {
            margin-right: 10px;
            font-size: 25px;
            color: #ee6059;
          }
      }
  }

}
  
</style>