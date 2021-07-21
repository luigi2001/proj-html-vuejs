<template>
  <section>
      <img @mouseover="hover = true" @mouseleave="hover = false" :src="require(`@/assets/${dettagli.img}`)" :alt="dettagli.img">
      <div class="hover" v-if="hover">
          <i class="fas fa-link bg-white p-3 rounded-circle"></i>
          <h3>{{dettagli.text}}</h3>
      </div>
  </section>
</template>

<script>
export default {
    name: 'CardImg',
    props: ["dettagli"],
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

    img{
      width: 300px;
    }

   .hover{
       font-size: 50px;
       position: absolute;
       left: 50%;
       top: 50%;
       transform: translate(-50%,-50%);
       h3{
           cursor: pointer;
           font-size: 16px;
           color: white;
       }

    }
}
</style>