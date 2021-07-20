<template>
  <section>
      <img @mouseover="hover = true" @mouseleave="hover = false" :src="require(`@/assets/${dettagli.img}`)" :alt="dettagli.text">
      <h4 class="mt-3">{{dettagli.text}}</h4>
      <p>By <a href="#">admin</a>|March 25th, 2019</p>
      <div class="hovereffect" v-if="hover">
          <i class="fas fa-link bg-white p-3 rounded-circle"></i>
          <h4>{{dettagli.text}}</h4>
      </div>
  </section>
</template>

<script>
export default {
    name: 'CardJambo',
    props:["dettagli"],
    data(){
        return{
            hover: false
        }
    }
}
</script>

<style lang="scss" scoped>
section{
    position: relative;
    h4{
        cursor: pointer;

        &:hover{
            color: #FC7523;
        }
    }
    p{
        color: gray;
        a{
            text-decoration: none;
            color: gray;

            &:hover{
                color: #FC7523;
            }
        }
    }
    img{
    width: 350px;
    }
    .hovereffect{
        font-size: 50px;
        position: absolute;
        left: 50%;
        top: 35%;
        transform: translate(-50%,-50%);
        h4{
        font-size: 16px;
        color: white;
        }
    }
}
</style>