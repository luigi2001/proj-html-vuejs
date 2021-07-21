<template>
  <section class="container">
      <h3 class="text-center">POPULAR RECIPES</h3>
      <p class="text-center">Aliquam erat volutpat. Ut quis ligula a magna blandit finibus. Suspendisse maximus lacus non nunc lacinia lobortis.</p>
      <div class="row mt-5">
          <div class="box col-6">
              <img @mouseover="hover = true" @mouseleave="hover = false" :src="require('@/assets/Yogurt-Nan.jpg')" alt="Yogurt Nan">
              <div class="hover text-center" v-if="hover">
                  <i class="fas fa-link bg-white p-3 rounded-circle"></i>
                  <h3>Lunch Favourite with Salad, Naan And Beans</h3>
              </div>
              <div class="descrizione p-4">
                  <h3>Lunch Favourite with Salad, Naan And Beans</h3>
                  <p class="border-bottom pb-3">Bakery, Featured, Healthy, Latest Recipes, Staff Picks</p>
                  <p>Suspendisse at semper odio. Nam fringilla scelerisque tincidunt. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Donec tincidunt posuere ornare. Phasellus placerat odio non feugiat sollicitudin. Integer vitae elementum ex. Sed porttitor, diam eget convallis volutpat, arcu tellus facilisis nulla, id dignissim orci leo id</p>
                  <button class="p-2 border-0">Learn More</button>
              </div>
          </div>
          <div class="col-6">
              <div class="row ms-2">
                  <div class="col-6 p-2 text-center" v-for="(item,index) in ArrayImg" :key="index">
                      <CardImg :dettagli="item"/>
                  </div>
              </div>
          </div>
      </div>
  </section>
</template>

<script>
import ArrayImg from '@/data/ArrayImg.js';
import CardImg from '@/components/CardImg.vue'
export default {
    name: 'SectionPopularRecipes',
    components:{
        CardImg
    },
    data(){
        return{
            ArrayImg: ArrayImg,
            hover: false
        }
    }
}
</script>

<style lang="scss" scoped>
.box{
    position: relative;
    background-color: white;
    h3{
        cursor: pointer;

        &:hover{
            color: #FC7523;
        }
    }
    img{
        width: 100%;
        height: 50%;
    }
    button{
        background-color: #FC7523;
        text-transform: uppercase;
        color: white;
    }
    .hover{
        font-size: 50px;
        position: absolute;
        left: 40%;
        top: 20%;
        transform: translate(-30%,-30%);
        h3{
            font-size: 16px;
            color: white;
        }
    }
}
</style>