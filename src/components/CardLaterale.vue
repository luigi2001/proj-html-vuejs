<template>
  <section class="ps-3">
      <div class="titleImg text-center">
          <a href="#"><img :src="require('@/assets/ad-bg.jpg')" alt="bg"></a>
          <h3>view our latest recipes</h3>
      </div>
      <div class="Singapore border-bottom pb-5">
          <a href="#"><img class="mt-3" :src="require('@/assets/singapore-featured-image.jpg')" alt="Singapore"></a>
          <h3 class="p-2">City Guide: Singapore</h3>
          <button class="p-2 border-0"> <i class="fas fa-globe-asia"></i> View All city guides</button>
      </div>
        <nav class="navbar pt-5 pb-5">
            <div class="container-fluid">
               <form class="d-flex">
                  <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
                </form>
            </div>
        </nav>
        <h6>Follow Us</h6>
        <div class="social mt-5">
          <a href="#"><i class="fab fa-facebook-f me-3"></i></a>
          <a href="#"><i class="fab fa-instagram me-3"></i></a>
          <a href="#"><i class="fab fa-twitter me-3"></i></a>
          <a href="#"><i class="fab fa-youtube me-3"></i></a>
        </div>
        <div class="titleList d-flex mt-5">
            <h5 class="p-3 bg-white border">Popular</h5>
            <h5 class="p-3 border">Recent</h5>
        </div>
        <div class="list d-flex mt-3" v-for="(list,index) in dettagli" :key="index">
            <a href="#"><img class="rounded-circle" :src="require(`@/assets/${list.img}`)" :alt="list.title"></a>
            <div class="descrizione ms-2">
                <h5>{{list.title}}</h5>
                <p>{{list.text}}</p>
            </div>
        </div>
  </section>
</template>

<script>
export default {
    name: 'CardLaterale',
    props:["dettagli"]
}
</script>

<style lang="scss" scoped>
section{
    img{
        width: 400px;
    }
    .titleImg{
        position: relative;
        text-transform: uppercase;
        h3{
            position: absolute;
            left: 50%;
            top: 50%;
            transform: translate(-50%,-50%);
        }
    }
    .Singapore{
        position: relative;
        h3{
            position: absolute;
            top: 60%;
            background-color: black;
            opacity: 0.7;
            color: white;
        }
        button{
            width: 100%;
            text-transform: uppercase;
            color: white;
            background-color: #FC7523;
        }
    }
    h6{
        color: #FC7523;
    }
    .social{
        a{
            margin-right: 50px;
            padding: 5px;
            font-size: 25px;
            color: gray;
            background-color: lightgray;
            border-radius: 10px;
        }
    }
    .list{
        img{
            width: 80px;
            height: 80px;
        }
        h5{
            cursor: pointer;

            &:hover{
                color: #FC7523;
            }
        }
    }
}
</style>