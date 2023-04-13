<template>
  <div>
    <header class="containerHeader">
      <div class="logo">
        <div class="containerImg">
         <a href="#"><img src="../assets/images/gym_logo_2x.png" alt=""> </a>
        </div>
      </div>
      <div class="link flex">
        <ul class="ul" v-for="(link,index) in links" :key="index">
          <li >
            <a :class="(link.active == true) ? 'active' : null" href="#">{{link.text}}</a>
          </li>
        </ul>
      </div>
    </header>
  </div>
    
</template>
  
<script>

export default {
  name: 'AppHeader',
  data(){
    return{
        links:[
        {
          text: 'HOME',
          url: '#',
          active: true
        },
        {
          text: 'ABOUT US',
          url: '#',
          active: false
        },
        {
          text: 'FACILITIES',
          url: '#',
          active: false
        },
        {
          text: 'MEMBERSHIP',
          url: '#',
          active: false
        },
        {
          text: 'TESTIMONIALS',
          url: '#',
          active: false
        },
        {
          text: 'BLOG',
          url: '#',
          active: false
        },

        ]
    }
  }
}
  </script>
  
<style lang="scss" scoped>
@import '../styles/generals.scss';
@import '../styles/variable.scss';

.containerHeader {
  width: 100%;
  height: 240px;
  display: flex;
    .logo {
      width: 50%;
      height: 100%;
      display: flex;
      align-items: center;
      padding: 100px;
        .containerImg {
          width: 170px;
          height: 100px;
            img {
              width: 100%;
              height: 100%;
            }
        }
    }
    .link {
      width: 50%;
      height: 100%;
        .ul {
          padding-right: 20px;
            li {
              list-style-type: none;
                a {
                  text-decoration: none;
                  color: $colorWhite;
                  font-size: 13px;
                }
                a.active {
                  color: $borderIcon;
                }
            }
        }
    }
}
  
  </style>