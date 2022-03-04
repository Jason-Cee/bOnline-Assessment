<template>
  <div class="container">
      <div class="nav_header">
          <div class="header_img">
              <img src="../assets/bOnline-New-Logo-PNG.png" alt="">
          </div>
          <div class="notification">
              <i class="fa-regular fa-bell"></i>
          </div>
      </div>
      <div class="profile">
          <img src="../assets/pp.jpg" alt="">
          <div class="profile_name">
                <h3>Lynda Monnoyer</h3>
                <p>lmonnoyer0@fema.gov</p>
          </div>
          <i class="fa-solid fa-angle-down"></i>
      </div>
  </div>
</template>

<script>
import Data from '../assets/Data.json'


export default {
  name: 'Nav',
  data(){
      return{
          data: Data
      }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
    .container{
        display: flex;
        width: 100vw;
        height: 5vh;
        background-color: #fff;
        border-bottom: #F0F0F0 1px solid;
    }

    .nav_header{
        display: flex;
        justify-content: space-between;
        width: 70%;
    }

    .header_img{
        height: 100%;
        width: 10%;
        display: flex;
        align-content: center;
    }

    .header_img img{
        width: 100%;
    }

    .notification{
     height: 100%;
     width: 3%;
     display:flex;
     justify-content: center;
     align-items: center;
     border-right: 1px solid #F0F0F0;
    }

    .profile{
        display: flex;
        justify-content: center;
        align-items: center;
        width: 20%;
        height: 90%;
    }

    .profile img{
        width: 50px;
        height: 100%;
        border-radius: 50%;
        margin-right: 10px;
    }

    .profile_name h3{
        font-size: 1rem;
    }

    .profile_name p{
        font-size: .7rem;
    }

    .profile i{
        margin-left: 10px;
    }
</style>
